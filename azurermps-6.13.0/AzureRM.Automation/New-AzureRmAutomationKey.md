---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 8bd043f11294b2290a5f54289232bc826c1f0d88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426453"
---
# <span data-ttu-id="7fc21-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="7fc21-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="7fc21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fc21-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc21-103">Regenera as chaves de registro para uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="7fc21-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fc21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fc21-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fc21-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fc21-105">DESCRIPTION</span></span>
<span data-ttu-id="7fc21-106">O cmdlet **New-AzureRmAutomationKey** regenera as chaves de registro para uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc21-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="7fc21-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fc21-107">EXAMPLES</span></span>

### <span data-ttu-id="7fc21-108">Exemplo 1: regenerar uma chave para uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="7fc21-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="7fc21-109">Esse comando regenera a chave primária da conta de automação do Azure chamada AutomationAccount01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7fc21-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="7fc21-110">OS</span><span class="sxs-lookup"><span data-stu-id="7fc21-110">PARAMETERS</span></span>

### <span data-ttu-id="7fc21-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7fc21-111">-AutomationAccountName</span></span>
<span data-ttu-id="7fc21-112">Especifica o nome de uma conta de automação para a qual esse cmdlet regenera as chaves.</span><span class="sxs-lookup"><span data-stu-id="7fc21-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="7fc21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc21-113">-DefaultProfile</span></span>
<span data-ttu-id="7fc21-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7fc21-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fc21-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="7fc21-115">-KeyType</span></span>
<span data-ttu-id="7fc21-116">Especifica o tipo da chave de registro do agente.</span><span class="sxs-lookup"><span data-stu-id="7fc21-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="7fc21-117">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="7fc21-117">Valid values are:</span></span> 
- <span data-ttu-id="7fc21-118">Preocupação</span><span class="sxs-lookup"><span data-stu-id="7fc21-118">Primary</span></span> 
- <span data-ttu-id="7fc21-119">Segundo</span><span class="sxs-lookup"><span data-stu-id="7fc21-119">Secondary</span></span>

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

### <span data-ttu-id="7fc21-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc21-120">-ResourceGroupName</span></span>
<span data-ttu-id="7fc21-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fc21-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7fc21-122">Esse cmdlet gera novamente chaves para uma conta de automação no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7fc21-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7fc21-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc21-123">CommonParameters</span></span>
<span data-ttu-id="7fc21-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fc21-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc21-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fc21-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc21-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fc21-126">INPUTS</span></span>

### <span data-ttu-id="7fc21-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7fc21-127">System.String</span></span>

## <span data-ttu-id="7fc21-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fc21-128">OUTPUTS</span></span>

### <span data-ttu-id="7fc21-129">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="7fc21-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="7fc21-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fc21-130">NOTES</span></span>

## <span data-ttu-id="7fc21-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fc21-131">RELATED LINKS</span></span>
