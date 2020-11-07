---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942671"
---
# <span data-ttu-id="b65b1-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="b65b1-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="b65b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b65b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b65b1-103">Obtém informações de registro para a integração de um nó DSC ou um trabalhador híbrido à automação.</span><span class="sxs-lookup"><span data-stu-id="b65b1-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="b65b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b65b1-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b65b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b65b1-105">DESCRIPTION</span></span>
<span data-ttu-id="b65b1-106">O cmdlet **Get-AzAutomationRegistrationInfo** Obtém o ponto de extremidade e as chaves necessárias para a integração de um nó de configuração de estado desejado (DSC) ou um trabalhador híbrido em uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="b65b1-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="b65b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b65b1-107">EXAMPLES</span></span>

### <span data-ttu-id="b65b1-108">Exemplo 1: obter informações de registro</span><span class="sxs-lookup"><span data-stu-id="b65b1-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="b65b1-109">Esse comando obtém as informações de registro da conta de automação chamada AutomationAccount01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b65b1-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="b65b1-110">OS</span><span class="sxs-lookup"><span data-stu-id="b65b1-110">PARAMETERS</span></span>

### <span data-ttu-id="b65b1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b65b1-111">-AutomationAccountName</span></span>
<span data-ttu-id="b65b1-112">Especifica o nome da conta de automação para a qual esse cmdlet obtém informações de registro.</span><span class="sxs-lookup"><span data-stu-id="b65b1-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65b1-113">-DefaultProfile</span></span>
<span data-ttu-id="b65b1-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b65b1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65b1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b65b1-115">-ResourceGroupName</span></span>
<span data-ttu-id="b65b1-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b65b1-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b65b1-117">Este cmdlet obtém informações de registro para o grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b65b1-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65b1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65b1-118">CommonParameters</span></span>
<span data-ttu-id="b65b1-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b65b1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65b1-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b65b1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65b1-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b65b1-121">INPUTS</span></span>

### <span data-ttu-id="b65b1-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b65b1-122">System.String</span></span>

## <span data-ttu-id="b65b1-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b65b1-123">OUTPUTS</span></span>

### <span data-ttu-id="b65b1-124">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="b65b1-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="b65b1-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b65b1-125">NOTES</span></span>

## <span data-ttu-id="b65b1-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b65b1-126">RELATED LINKS</span></span>

[<span data-ttu-id="b65b1-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b65b1-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="b65b1-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b65b1-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="b65b1-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="b65b1-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


