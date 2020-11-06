---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: d40e79e53ccf2ddd9cb5c251328268da0bed76fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602884"
---
# <span data-ttu-id="90401-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="90401-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="90401-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90401-102">SYNOPSIS</span></span>
<span data-ttu-id="90401-103">Cria uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="90401-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90401-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90401-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90401-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90401-105">DESCRIPTION</span></span>
<span data-ttu-id="90401-106">O cmdlet **New-AzureRmAutomationAccount** cria uma conta de automação do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="90401-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="90401-107">Uma conta de automação é um contêiner de recursos de automação que é isolado dos recursos de outras contas de automação.</span><span class="sxs-lookup"><span data-stu-id="90401-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="90401-108">Os recursos de automação incluem runbooks, configurações de estado desejado (DSC), trabalhos e ativos.</span><span class="sxs-lookup"><span data-stu-id="90401-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="90401-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90401-109">EXAMPLES</span></span>

### <span data-ttu-id="90401-110">Exemplo 1: criar uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="90401-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="90401-111">Esse comando cria uma nova conta de automação chamada ContosoAutomationAccount na região leste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="90401-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="90401-112">OS</span><span class="sxs-lookup"><span data-stu-id="90401-112">PARAMETERS</span></span>

### <span data-ttu-id="90401-113">-Local</span><span class="sxs-lookup"><span data-stu-id="90401-113">-Location</span></span>
<span data-ttu-id="90401-114">Especifica o local em que esse cmdlet cria a conta de automação.</span><span class="sxs-lookup"><span data-stu-id="90401-114">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="90401-115">Para obter locais válidos, use o cmdlet Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="90401-115">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="90401-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="90401-116">-Name</span></span>
<span data-ttu-id="90401-117">Especifica um nome para a conta de automação.</span><span class="sxs-lookup"><span data-stu-id="90401-117">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="90401-118">-Plano</span><span class="sxs-lookup"><span data-stu-id="90401-118">-Plan</span></span>
<span data-ttu-id="90401-119">Especifica o plano para a conta de automação.</span><span class="sxs-lookup"><span data-stu-id="90401-119">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="90401-120">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="90401-120">Valid values are:</span></span>

- <span data-ttu-id="90401-121">Basic</span><span class="sxs-lookup"><span data-stu-id="90401-121">Basic</span></span>
- <span data-ttu-id="90401-122">Gratuito</span><span class="sxs-lookup"><span data-stu-id="90401-122">Free</span></span>

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

### <span data-ttu-id="90401-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90401-123">-ResourceGroupName</span></span>
<span data-ttu-id="90401-124">Especifica o nome de um grupo de recursos para o qual esse cmdlet adiciona uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="90401-124">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="90401-125">-Marcas</span><span class="sxs-lookup"><span data-stu-id="90401-125">-Tags</span></span>
<span data-ttu-id="90401-126">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="90401-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="90401-127">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="90401-127">For example:</span></span>

<span data-ttu-id="90401-128">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="90401-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="90401-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90401-129">-DefaultProfile</span></span>
<span data-ttu-id="90401-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90401-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90401-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90401-131">CommonParameters</span></span>
<span data-ttu-id="90401-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90401-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90401-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90401-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90401-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90401-134">INPUTS</span></span>

## <span data-ttu-id="90401-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90401-135">OUTPUTS</span></span>

### <span data-ttu-id="90401-136">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="90401-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="90401-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90401-137">NOTES</span></span>

## <span data-ttu-id="90401-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90401-138">RELATED LINKS</span></span>

[<span data-ttu-id="90401-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="90401-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="90401-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="90401-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="90401-141">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="90401-141">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
