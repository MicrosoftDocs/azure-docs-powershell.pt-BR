---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: 3116ee67b55df50d4dc79df2ee3faef3823878b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889703"
---
# <span data-ttu-id="1f3e6-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="1f3e6-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="1f3e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3e6-103">Regenera as chaves de registro de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="1f3e6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1f3e6-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f3e6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1f3e6-105">DESCRIPTION</span></span>
<span data-ttu-id="1f3e6-106">O cmdlet **New-AzAutomationKey** regenera as chaves de registro de uma conta de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="1f3e6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f3e6-107">EXAMPLES</span></span>

### <span data-ttu-id="1f3e6-108">Exemplo 1: Regenerar uma chave para uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="1f3e6-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="1f3e6-109">Este comando regenera a chave primária da conta de Automação do Azure chamada AutomationAccount01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="1f3e6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1f3e6-110">PARAMETERS</span></span>

### <span data-ttu-id="1f3e6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f3e6-111">-AutomationAccountName</span></span>
<span data-ttu-id="1f3e6-112">Especifica o nome de uma conta de automação para a qual esse cmdlet regenera chaves.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="1f3e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3e6-113">-DefaultProfile</span></span>
<span data-ttu-id="1f3e6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1f3e6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f3e6-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1f3e6-115">-KeyType</span></span>
<span data-ttu-id="1f3e6-116">Especifica o tipo da chave de registro do agente.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="1f3e6-117">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1f3e6-117">Valid values are:</span></span> 
- <span data-ttu-id="1f3e6-118">Primário</span><span class="sxs-lookup"><span data-stu-id="1f3e6-118">Primary</span></span> 
- <span data-ttu-id="1f3e6-119">Secundário</span><span class="sxs-lookup"><span data-stu-id="1f3e6-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3e6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f3e6-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f3e6-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1f3e6-122">Este cmdlet regenera chaves para uma conta de Automação no grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1f3e6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3e6-123">CommonParameters</span></span>
<span data-ttu-id="1f3e6-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3e6-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f3e6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3e6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f3e6-126">INPUTS</span></span>

### <span data-ttu-id="1f3e6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1f3e6-127">System.String</span></span>

## <span data-ttu-id="1f3e6-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1f3e6-128">OUTPUTS</span></span>

### <span data-ttu-id="1f3e6-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="1f3e6-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="1f3e6-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="1f3e6-130">NOTES</span></span>

## <span data-ttu-id="1f3e6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f3e6-131">RELATED LINKS</span></span>
