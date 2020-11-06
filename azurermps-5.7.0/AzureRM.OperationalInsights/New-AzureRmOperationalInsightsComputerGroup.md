---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 999e9e5fd9f0b93e71b222f228b1575e0492073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440098"
---
# <span data-ttu-id="798e5-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="798e5-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="798e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="798e5-102">SYNOPSIS</span></span>
<span data-ttu-id="798e5-103">Cria um grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="798e5-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="798e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="798e5-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="798e5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="798e5-105">DESCRIPTION</span></span>
<span data-ttu-id="798e5-106">O cmdlet **New-AzureRmOperationalInsightsComputerGroup** cria um grupo de computadores em um grupo de recursos e local.</span><span class="sxs-lookup"><span data-stu-id="798e5-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="798e5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="798e5-107">EXAMPLES</span></span>

## <span data-ttu-id="798e5-108">OS</span><span class="sxs-lookup"><span data-stu-id="798e5-108">PARAMETERS</span></span>

### <span data-ttu-id="798e5-109">-Categoria</span><span class="sxs-lookup"><span data-stu-id="798e5-109">-Category</span></span>
<span data-ttu-id="798e5-110">Especifica a categoria do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="798e5-110">Specifies the category of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798e5-111">-DefaultProfile</span></span>
<span data-ttu-id="798e5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="798e5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="798e5-113">-DisplayName</span></span>
<span data-ttu-id="798e5-114">Especifica o nome de exibição do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="798e5-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="798e5-115">-Force</span></span>
<span data-ttu-id="798e5-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="798e5-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-117">-Consulta</span><span class="sxs-lookup"><span data-stu-id="798e5-117">-Query</span></span>
<span data-ttu-id="798e5-118">Especifica a consulta do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="798e5-118">Specifies the query of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="798e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="798e5-120">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="798e5-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="798e5-121">O cmdlet cria um grupo de computadores nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="798e5-121">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="798e5-122">-SavedSearchId</span></span>
<span data-ttu-id="798e5-123">Especifica a ID do grupo de computadores.</span><span class="sxs-lookup"><span data-stu-id="798e5-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-124">-Versão</span><span class="sxs-lookup"><span data-stu-id="798e5-124">-Version</span></span>
<span data-ttu-id="798e5-125">Especifica a versão.</span><span class="sxs-lookup"><span data-stu-id="798e5-125">Specifies the version.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="798e5-126">-WorkspaceName</span></span>
<span data-ttu-id="798e5-127">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="798e5-127">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="798e5-128">-Confirm</span></span>
<span data-ttu-id="798e5-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="798e5-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="798e5-130">-WhatIf</span></span>
<span data-ttu-id="798e5-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="798e5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="798e5-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="798e5-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798e5-133">CommonParameters</span></span>
<span data-ttu-id="798e5-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="798e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="798e5-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="798e5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798e5-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="798e5-136">INPUTS</span></span>

### <span data-ttu-id="798e5-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="798e5-137">None</span></span>
<span data-ttu-id="798e5-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="798e5-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="798e5-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="798e5-139">OUTPUTS</span></span>

## <span data-ttu-id="798e5-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="798e5-140">NOTES</span></span>

## <span data-ttu-id="798e5-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="798e5-141">RELATED LINKS</span></span>

