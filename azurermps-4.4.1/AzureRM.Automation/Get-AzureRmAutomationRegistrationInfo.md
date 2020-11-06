---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: 2ab7feb754bce7b160bf5aa47e225160649a70ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431188"
---
# <span data-ttu-id="0c175-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="0c175-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="0c175-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c175-102">SYNOPSIS</span></span>
<span data-ttu-id="0c175-103">Obtém informações de registro para a integração de um nó DSC ou um trabalhador híbrido à automação.</span><span class="sxs-lookup"><span data-stu-id="0c175-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c175-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c175-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c175-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c175-105">DESCRIPTION</span></span>
<span data-ttu-id="0c175-106">O cmdlet **Get-AzureRmAutomationRegistrationInfo** Obtém o ponto de extremidade e as chaves necessárias para a integração de um nó de configuração de estado desejado (DSC) ou um trabalhador híbrido em uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c175-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="0c175-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c175-107">EXAMPLES</span></span>

### <span data-ttu-id="0c175-108">Exemplo 1: obter informações de registro</span><span class="sxs-lookup"><span data-stu-id="0c175-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="0c175-109">Esse comando obtém as informações de registro da conta de automação chamada AutomationAccount01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0c175-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="0c175-110">OS</span><span class="sxs-lookup"><span data-stu-id="0c175-110">PARAMETERS</span></span>

### <span data-ttu-id="0c175-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0c175-111">-AutomationAccountName</span></span>
<span data-ttu-id="0c175-112">Especifica o nome da conta de automação para a qual esse cmdlet obtém informações de registro.</span><span class="sxs-lookup"><span data-stu-id="0c175-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="0c175-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c175-113">-ResourceGroupName</span></span>
<span data-ttu-id="0c175-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c175-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0c175-115">Este cmdlet obtém informações de registro para o grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="0c175-115">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c175-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c175-116">-DefaultProfile</span></span>
<span data-ttu-id="0c175-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c175-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c175-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c175-118">CommonParameters</span></span>
<span data-ttu-id="0c175-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c175-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c175-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c175-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c175-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c175-121">INPUTS</span></span>

## <span data-ttu-id="0c175-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c175-122">OUTPUTS</span></span>

### <span data-ttu-id="0c175-123">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="0c175-123">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="0c175-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c175-124">NOTES</span></span>

## <span data-ttu-id="0c175-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c175-125">RELATED LINKS</span></span>

[<span data-ttu-id="0c175-126">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0c175-126">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="0c175-127">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0c175-127">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="0c175-128">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="0c175-128">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


