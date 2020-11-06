---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: 84332967eadfdb2accd12cc2f6f840ee337f92ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427315"
---
# <span data-ttu-id="5460a-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="5460a-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="5460a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5460a-102">SYNOPSIS</span></span>
<span data-ttu-id="5460a-103">Obtém informações de registro para a integração de um nó DSC ou um trabalhador híbrido à automação.</span><span class="sxs-lookup"><span data-stu-id="5460a-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5460a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5460a-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5460a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5460a-105">DESCRIPTION</span></span>
<span data-ttu-id="5460a-106">O cmdlet **Get-AzureRmAutomationRegistrationInfo** Obtém o ponto de extremidade e as chaves necessárias para a integração de um nó de configuração de estado desejado (DSC) ou um trabalhador híbrido em uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="5460a-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="5460a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5460a-107">EXAMPLES</span></span>

### <span data-ttu-id="5460a-108">Exemplo 1: obter informações de registro</span><span class="sxs-lookup"><span data-stu-id="5460a-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="5460a-109">Esse comando obtém as informações de registro da conta de automação chamada AutomationAccount01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="5460a-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="5460a-110">OS</span><span class="sxs-lookup"><span data-stu-id="5460a-110">PARAMETERS</span></span>

### <span data-ttu-id="5460a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5460a-111">-AutomationAccountName</span></span>
<span data-ttu-id="5460a-112">Especifica o nome da conta de automação para a qual esse cmdlet obtém informações de registro.</span><span class="sxs-lookup"><span data-stu-id="5460a-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="5460a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5460a-113">-DefaultProfile</span></span>
<span data-ttu-id="5460a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5460a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5460a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5460a-115">-ResourceGroupName</span></span>
<span data-ttu-id="5460a-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5460a-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5460a-117">Este cmdlet obtém informações de registro para o grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5460a-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5460a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5460a-118">CommonParameters</span></span>
<span data-ttu-id="5460a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5460a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5460a-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5460a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5460a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5460a-121">INPUTS</span></span>

### <span data-ttu-id="5460a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5460a-122">System.String</span></span>

## <span data-ttu-id="5460a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5460a-123">OUTPUTS</span></span>

### <span data-ttu-id="5460a-124">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="5460a-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="5460a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5460a-125">NOTES</span></span>

## <span data-ttu-id="5460a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5460a-126">RELATED LINKS</span></span>

[<span data-ttu-id="5460a-127">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5460a-127">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="5460a-128">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="5460a-128">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="5460a-129">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="5460a-129">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


