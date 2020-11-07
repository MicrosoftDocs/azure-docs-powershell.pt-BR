---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: d1a1633303e30fc10c5eee7432101fa075f4d38f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772885"
---
# <span data-ttu-id="f849e-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="f849e-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="f849e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f849e-102">SYNOPSIS</span></span>
<span data-ttu-id="f849e-103">Cria um grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="f849e-103">Creates a computer group.</span></span>

## <span data-ttu-id="f849e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f849e-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f849e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f849e-105">DESCRIPTION</span></span>
<span data-ttu-id="f849e-106">O cmdlet **New-AzOperationalInsightsComputerGroup** cria um grupo de computadores em um grupo de recursos e local.</span><span class="sxs-lookup"><span data-stu-id="f849e-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="f849e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f849e-107">EXAMPLES</span></span>

## <span data-ttu-id="f849e-108">OS</span><span class="sxs-lookup"><span data-stu-id="f849e-108">PARAMETERS</span></span>

### <span data-ttu-id="f849e-109">-Categoria</span><span class="sxs-lookup"><span data-stu-id="f849e-109">-Category</span></span>
<span data-ttu-id="f849e-110">Especifica a categoria do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="f849e-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="f849e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f849e-111">-DefaultProfile</span></span>
<span data-ttu-id="f849e-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f849e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f849e-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f849e-113">-DisplayName</span></span>
<span data-ttu-id="f849e-114">Especifica o nome de exibição do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="f849e-114">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="f849e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f849e-115">-Force</span></span>
<span data-ttu-id="f849e-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f849e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f849e-117">-Consulta</span><span class="sxs-lookup"><span data-stu-id="f849e-117">-Query</span></span>
<span data-ttu-id="f849e-118">Especifica a consulta do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="f849e-118">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="f849e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f849e-119">-ResourceGroupName</span></span>
<span data-ttu-id="f849e-120">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f849e-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f849e-121">O cmdlet cria um grupo de computadores nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f849e-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="f849e-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="f849e-122">-SavedSearchId</span></span>
<span data-ttu-id="f849e-123">Especifica a ID do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="f849e-123">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="f849e-124">-Versão</span><span class="sxs-lookup"><span data-stu-id="f849e-124">-Version</span></span>
<span data-ttu-id="f849e-125">Especifica a versão.</span><span class="sxs-lookup"><span data-stu-id="f849e-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f849e-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f849e-126">-WorkspaceName</span></span>
<span data-ttu-id="f849e-127">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f849e-127">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="f849e-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f849e-128">-Confirm</span></span>
<span data-ttu-id="f849e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f849e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f849e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f849e-130">-WhatIf</span></span>
<span data-ttu-id="f849e-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f849e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f849e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f849e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f849e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f849e-133">CommonParameters</span></span>
<span data-ttu-id="f849e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f849e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f849e-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f849e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f849e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f849e-136">INPUTS</span></span>

### <span data-ttu-id="f849e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f849e-137">System.String</span></span>

### <span data-ttu-id="f849e-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="f849e-138">System.Int64</span></span>

## <span data-ttu-id="f849e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f849e-139">OUTPUTS</span></span>

### <span data-ttu-id="f849e-140">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="f849e-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="f849e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f849e-141">NOTES</span></span>

## <span data-ttu-id="f849e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f849e-142">RELATED LINKS</span></span>
