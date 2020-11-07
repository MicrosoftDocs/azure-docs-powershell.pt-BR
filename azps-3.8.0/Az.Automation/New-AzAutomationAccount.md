---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 350e1591081e1d171921a432a1b990066614c750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944978"
---
# <span data-ttu-id="ca267-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ca267-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="ca267-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca267-102">SYNOPSIS</span></span>
<span data-ttu-id="ca267-103">Cria uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ca267-103">Creates an Automation account.</span></span>

## <span data-ttu-id="ca267-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca267-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca267-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca267-105">DESCRIPTION</span></span>
<span data-ttu-id="ca267-106">O cmdlet **New-AzAutomationAccount** cria uma conta de automação do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca267-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="ca267-107">Uma conta de automação é um contêiner de recursos de automação que é isolado dos recursos de outras contas de automação.</span><span class="sxs-lookup"><span data-stu-id="ca267-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="ca267-108">Os recursos de automação incluem runbooks, configurações de estado desejado (DSC), trabalhos e ativos.</span><span class="sxs-lookup"><span data-stu-id="ca267-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="ca267-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca267-109">EXAMPLES</span></span>

### <span data-ttu-id="ca267-110">Exemplo 1: criar uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="ca267-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ca267-111">Esse comando cria uma nova conta de automação chamada ContosoAutomationAccount na região leste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="ca267-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="ca267-112">OS</span><span class="sxs-lookup"><span data-stu-id="ca267-112">PARAMETERS</span></span>

### <span data-ttu-id="ca267-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca267-113">-DefaultProfile</span></span>
<span data-ttu-id="ca267-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ca267-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca267-115">-Local</span><span class="sxs-lookup"><span data-stu-id="ca267-115">-Location</span></span>
<span data-ttu-id="ca267-116">Especifica o local em que esse cmdlet cria a conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ca267-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="ca267-117">Para obter locais válidos, use o cmdlet Get-AzLocation.</span><span class="sxs-lookup"><span data-stu-id="ca267-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca267-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca267-118">-Name</span></span>
<span data-ttu-id="ca267-119">Especifica um nome para a conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ca267-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca267-120">-Plano</span><span class="sxs-lookup"><span data-stu-id="ca267-120">-Plan</span></span>
<span data-ttu-id="ca267-121">Especifica o plano para a conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ca267-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="ca267-122">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="ca267-122">Valid values are:</span></span>
- <span data-ttu-id="ca267-123">Basic</span><span class="sxs-lookup"><span data-stu-id="ca267-123">Basic</span></span>
- <span data-ttu-id="ca267-124">Gratuito</span><span class="sxs-lookup"><span data-stu-id="ca267-124">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca267-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca267-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca267-126">Especifica o nome de um grupo de recursos para o qual esse cmdlet adiciona uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ca267-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="ca267-127">-Marcas</span><span class="sxs-lookup"><span data-stu-id="ca267-127">-Tags</span></span>
<span data-ttu-id="ca267-128">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ca267-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ca267-129">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ca267-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca267-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca267-130">CommonParameters</span></span>
<span data-ttu-id="ca267-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca267-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca267-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca267-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca267-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca267-133">INPUTS</span></span>

### <span data-ttu-id="ca267-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ca267-134">System.String</span></span>

### <span data-ttu-id="ca267-135">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="ca267-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="ca267-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca267-136">OUTPUTS</span></span>

### <span data-ttu-id="ca267-137">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ca267-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="ca267-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca267-138">NOTES</span></span>

## <span data-ttu-id="ca267-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca267-139">RELATED LINKS</span></span>

[<span data-ttu-id="ca267-140">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ca267-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="ca267-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ca267-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="ca267-142">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ca267-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
