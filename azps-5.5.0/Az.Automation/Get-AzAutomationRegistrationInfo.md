---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116632"
---
# <span data-ttu-id="fd183-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="fd183-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="fd183-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd183-102">SYNOPSIS</span></span>
<span data-ttu-id="fd183-103">Obtém informações de registro para integração de um nó DSC ou de um trabalhador híbrido à Automação.</span><span class="sxs-lookup"><span data-stu-id="fd183-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="fd183-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd183-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd183-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd183-105">DESCRIPTION</span></span>
<span data-ttu-id="fd183-106">O cmdlet **Get-AzAutomationRegistrationInfo** obtém o ponto de extremidade e as teclas necessárias para integrar um nó DSC (Configuração de Estado Desejado) ou um trabalhador híbrido em uma conta de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="fd183-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="fd183-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd183-107">EXAMPLES</span></span>

### <span data-ttu-id="fd183-108">Exemplo 1: Obter informações de registro</span><span class="sxs-lookup"><span data-stu-id="fd183-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="fd183-109">Esse comando obtém as informações de registro da conta automação chamada AutomationAccount01 no Grupo de Recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fd183-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="fd183-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd183-110">PARAMETERS</span></span>

### <span data-ttu-id="fd183-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd183-111">-AutomationAccountName</span></span>
<span data-ttu-id="fd183-112">Especifica o nome da conta automação para a qual este cmdlet obtém informações de registro.</span><span class="sxs-lookup"><span data-stu-id="fd183-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="fd183-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd183-113">-DefaultProfile</span></span>
<span data-ttu-id="fd183-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fd183-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd183-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd183-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd183-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd183-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="fd183-117">Este cmdlet obtém informações de registro para o grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fd183-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fd183-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd183-118">CommonParameters</span></span>
<span data-ttu-id="fd183-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd183-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd183-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd183-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd183-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd183-121">INPUTS</span></span>

### <span data-ttu-id="fd183-122">System.String</span><span class="sxs-lookup"><span data-stu-id="fd183-122">System.String</span></span>

## <span data-ttu-id="fd183-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd183-123">OUTPUTS</span></span>

### <span data-ttu-id="fd183-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="fd183-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="fd183-125">Notas</span><span class="sxs-lookup"><span data-stu-id="fd183-125">NOTES</span></span>

## <span data-ttu-id="fd183-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd183-126">RELATED LINKS</span></span>

[<span data-ttu-id="fd183-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fd183-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="fd183-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="fd183-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="fd183-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="fd183-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


