---
title: '연습: XAML을 사용하여 WPF에서 Windows Forms 컨트롤 호스팅'
ms.date: 03/30/2017
helpviewer_keywords:
- hosting Windows Forms control in WPF [WPF]
ms.assetid: 1aef42cb-4cfb-44b4-9a7a-c02632d3d9c7
ms.openlocfilehash: 2f13689a15e91ee0f80c0d7b6bc71c5f973b8333
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44083870"
---
# <a name="walkthrough-hosting-a-windows-forms-control-in-wpf-by-using-xaml"></a>연습: XAML을 사용하여 WPF에서 Windows Forms 컨트롤 호스팅
[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]에서는 풍부한 기능 집합이 있는 많은 컨트롤을 제공합니다. 그러나 사용 하려는 경우에 따라 [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] 컨트롤에 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] 페이지입니다. 예를 들어, 기존에 상당한 투자를 해야 [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] 컨트롤 또는 있습니다 있을 [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] 고유한 기능을 제공 하는 컨트롤입니다.  
  
 이 연습에서는 Windows Forms를 호스트 하는 방법을 보여 줍니다 <xref:System.Windows.Forms.MaskedTextBox?displayProperty=nameWithType> 컨트롤을 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] 페이지를 사용 하 여 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]입니다.  
  
 이 연습에 나와 있는 작업의 전체 코드 목록은 참조 하세요 [XAML 예제를 사용 하 여 WPF에서 Windows Forms 컨트롤 호스팅](https://go.microsoft.com/fwlink/?LinkID=160000)합니다.  
  
## <a name="prerequisites"></a>전제 조건  
 이 연습을 완료하려면 다음 구성 요소가 필요합니다.  
  
-   [!INCLUDE[vs_dev10_long](../../../../includes/vs-dev10-long-md.md)].  
  
## <a name="hosting-the-windows-forms-control"></a>Windows Forms 컨트롤 호스팅  
  
#### <a name="to-host-the-maskedtextbox-control"></a>MaskedTextBox 컨트롤을 호스트하려면  
  
1.  이라는 WPF 응용 프로그램 프로젝트를 만듭니다 `HostingWfInWpfWithXaml`합니다.  
  
2.  다음 어셈블리에 대한 참조를 추가합니다.  
  
    -   WindowsFormsIntegration  
  
    -   System.Windows.Forms  
  
3.  MainWindow.xaml을 엽니다는 [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)]합니다.  
  
4.  에 <xref:System.Windows.Window> 요소를 다음 네임 스페이스 매핑을 추가 합니다. `wf` 네임 스페이스 매핑 Windows Forms 컨트롤을 포함 하는 어셈블리에 대 한 참조를 설정 합니다.  
  
    ```xaml  
    xmlns:wf="clr-namespace:System.Windows.Forms;assembly=System.Windows.Forms"  
    ```  
  
5.  에 <xref:System.Windows.Controls.Grid> 다음 XAML을 추가 하는 요소입니다.  
  
     합니다 <xref:System.Windows.Forms.MaskedTextBox> 컨트롤의 자식으로 생성 됩니다는 <xref:System.Windows.Forms.Integration.WindowsFormsHost> 제어 합니다.  
  
     [!code-xaml[HostingWfInWpfWithXaml#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWfInWpfWithXaml/CSharp/HostingWfInWpf/Window1.xaml#3)]  
  
6.  F5 키를 눌러 응용 프로그램을 빌드하고 실행합니다.  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 [Visual Studio에서 XAML 디자인](/visualstudio/designers/designing-xaml-in-visual-studio)  
 [연습: WPF에서 Windows Forms 컨트롤 호스팅](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf.md)  
 [연습: WPF에서 Windows Forms 복합 컨트롤 호스팅](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)  
 [연습: Windows Forms에서 WPF 복합 컨트롤 호스팅](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)  
 [Windows Forms 컨트롤 및 해당 WPF 컨트롤](../../../../docs/framework/wpf/advanced/windows-forms-controls-and-equivalent-wpf-controls.md)  
 [XAML 샘플을 사용 하 여 WPF에서 Windows Forms 컨트롤 호스팅](https://go.microsoft.com/fwlink/?LinkID=160000)
