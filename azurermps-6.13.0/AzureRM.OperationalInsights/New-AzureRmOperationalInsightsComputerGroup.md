---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 60c1db3595c3ca33676fbd874356376981a72407
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428430"
---
# <span data-ttu-id="19539-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="19539-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="19539-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19539-102">SYNOPSIS</span></span>
<span data-ttu-id="19539-103">Cria um grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="19539-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19539-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19539-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19539-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19539-105">DESCRIPTION</span></span>
<span data-ttu-id="19539-106">O cmdlet **New-AzureRmOperationalInsightsComputerGroup** cria um grupo de computadores em um grupo de recursos e local.</span><span class="sxs-lookup"><span data-stu-id="19539-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="19539-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19539-107">EXAMPLES</span></span>

## <span data-ttu-id="19539-108">OS</span><span class="sxs-lookup"><span data-stu-id="19539-108">PARAMETERS</span></span>

### <span data-ttu-id="19539-109">-Categoria</span><span class="sxs-lookup"><span data-stu-id="19539-109">-Category</span></span>
<span data-ttu-id="19539-110">Especifica a categoria do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="19539-110">Specifies the category of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19539-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19539-111">-DefaultProfile</span></span>
<span data-ttu-id="19539-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="19539-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19539-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="19539-113">-DisplayName</span></span>
<span data-ttu-id="19539-114">Especifica o nome de exibição do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="19539-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19539-115">-Force</span><span class="sxs-lookup"><span data-stu-id="19539-115">-Force</span></span>
<span data-ttu-id="19539-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="19539-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19539-117">-Consulta</span><span class="sxs-lookup"><span data-stu-id="19539-117">-Query</span></span>
<span data-ttu-id="19539-118">Especifica a consulta do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="19539-118">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19539-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19539-119">-ResourceGroupName</span></span>
<span data-ttu-id="19539-120">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="19539-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="19539-121">O cmdlet cria um grupo de computadores nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19539-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="19539-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="19539-122">-SavedSearchId</span></span>
<span data-ttu-id="19539-123">Especifica a ID do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="19539-123">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="19539-124">-Versão</span><span class="sxs-lookup"><span data-stu-id="19539-124">-Version</span></span>
<span data-ttu-id="19539-125">Especifica a versão.</span><span class="sxs-lookup"><span data-stu-id="19539-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19539-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="19539-126">-WorkspaceName</span></span>
<span data-ttu-id="19539-127">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="19539-127">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19539-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19539-128">-Confirm</span></span>
<span data-ttu-id="19539-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19539-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19539-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19539-130">-WhatIf</span></span>
<span data-ttu-id="19539-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19539-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19539-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19539-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19539-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19539-133">CommonParameters</span></span>
<span data-ttu-id="19539-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19539-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19539-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19539-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19539-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19539-136">INPUTS</span></span>

### <span data-ttu-id="19539-137">System. String</span><span class="sxs-lookup"><span data-stu-id="19539-137">System.String</span></span>

### <span data-ttu-id="19539-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="19539-138">System.Int64</span></span>

## <span data-ttu-id="19539-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19539-139">OUTPUTS</span></span>

### <span data-ttu-id="19539-140">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="19539-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="19539-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19539-141">NOTES</span></span>

## <span data-ttu-id="19539-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19539-142">RELATED LINKS</span></span>
