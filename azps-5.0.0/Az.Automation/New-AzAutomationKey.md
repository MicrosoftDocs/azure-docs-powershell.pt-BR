---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281486"
---
# <span data-ttu-id="62116-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="62116-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="62116-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62116-102">SYNOPSIS</span></span>
<span data-ttu-id="62116-103">Regenera as chaves de registro para uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="62116-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="62116-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62116-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62116-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62116-105">DESCRIPTION</span></span>
<span data-ttu-id="62116-106">O cmdlet **New-AzAutomationKey** regenera as chaves de registro para uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="62116-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="62116-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62116-107">EXAMPLES</span></span>

### <span data-ttu-id="62116-108">Exemplo 1: regenerar uma chave para uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="62116-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="62116-109">Esse comando regenera a chave primária da conta de automação do Azure chamada AutomationAccount01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="62116-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="62116-110">OS</span><span class="sxs-lookup"><span data-stu-id="62116-110">PARAMETERS</span></span>

### <span data-ttu-id="62116-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="62116-111">-AutomationAccountName</span></span>
<span data-ttu-id="62116-112">Especifica o nome de uma conta de automação para a qual esse cmdlet regenera as chaves.</span><span class="sxs-lookup"><span data-stu-id="62116-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="62116-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62116-113">-DefaultProfile</span></span>
<span data-ttu-id="62116-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="62116-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62116-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="62116-115">-KeyType</span></span>
<span data-ttu-id="62116-116">Especifica o tipo da chave de registro do agente.</span><span class="sxs-lookup"><span data-stu-id="62116-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="62116-117">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="62116-117">Valid values are:</span></span> 
- <span data-ttu-id="62116-118">Preocupação</span><span class="sxs-lookup"><span data-stu-id="62116-118">Primary</span></span> 
- <span data-ttu-id="62116-119">Segundo</span><span class="sxs-lookup"><span data-stu-id="62116-119">Secondary</span></span>

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

### <span data-ttu-id="62116-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62116-120">-ResourceGroupName</span></span>
<span data-ttu-id="62116-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62116-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="62116-122">Esse cmdlet gera novamente chaves para uma conta de automação no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="62116-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="62116-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62116-123">CommonParameters</span></span>
<span data-ttu-id="62116-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62116-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62116-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62116-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62116-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62116-126">INPUTS</span></span>

### <span data-ttu-id="62116-127">System. String</span><span class="sxs-lookup"><span data-stu-id="62116-127">System.String</span></span>

## <span data-ttu-id="62116-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62116-128">OUTPUTS</span></span>

### <span data-ttu-id="62116-129">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="62116-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="62116-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62116-130">NOTES</span></span>

## <span data-ttu-id="62116-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62116-131">RELATED LINKS</span></span>
