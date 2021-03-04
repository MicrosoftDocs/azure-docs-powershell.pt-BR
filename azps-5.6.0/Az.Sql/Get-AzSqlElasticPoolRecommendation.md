---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 03f2d7b9ae97282d0144ca19b493081fd2d8d774
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891591"
---
# <span data-ttu-id="5de21-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="5de21-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="5de21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5de21-102">SYNOPSIS</span></span>
<span data-ttu-id="5de21-103">Obtém recomendações de pool elástica.</span><span class="sxs-lookup"><span data-stu-id="5de21-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="5de21-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5de21-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5de21-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5de21-105">DESCRIPTION</span></span>
<span data-ttu-id="5de21-106">O cmdlet **Get-AzSqlElasticPoolRecommendation** obtém recomendações de pool elásticas para um servidor.</span><span class="sxs-lookup"><span data-stu-id="5de21-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="5de21-107">Essas recomendações incluem os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5de21-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="5de21-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="5de21-108">DatabaseCollection.</span></span> <span data-ttu-id="5de21-109">Coleção de nomes de banco de dados que pertencem ao pool.</span><span class="sxs-lookup"><span data-stu-id="5de21-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="5de21-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="5de21-110">DatabaseDtuMin.</span></span> <span data-ttu-id="5de21-111">Garantia da Unidade de Transmissão de Dados (DTU) para bancos de dados no pool elástica.</span><span class="sxs-lookup"><span data-stu-id="5de21-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="5de21-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="5de21-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="5de21-113">Limite de DTU para bancos de dados no pool elástica.</span><span class="sxs-lookup"><span data-stu-id="5de21-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="5de21-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="5de21-114">Dtu.</span></span> <span data-ttu-id="5de21-115">Garantia de DTU para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="5de21-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="5de21-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="5de21-116">StorageMb.</span></span> <span data-ttu-id="5de21-117">Armazenamento em megabytes para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="5de21-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="5de21-118">Edição.</span><span class="sxs-lookup"><span data-stu-id="5de21-118">Edition.</span></span> <span data-ttu-id="5de21-119">Edição para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="5de21-119">Edition for the elastic pool.</span></span> <span data-ttu-id="5de21-120">Os valores aceitáveis para este parâmetro são: Básico, Padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="5de21-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="5de21-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="5de21-121">IncludeAllDatabases.</span></span> <span data-ttu-id="5de21-122">Indica se todos os bancos de dados no pool elástica são retornados.</span><span class="sxs-lookup"><span data-stu-id="5de21-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="5de21-123">Nome.</span><span class="sxs-lookup"><span data-stu-id="5de21-123">Name.</span></span> <span data-ttu-id="5de21-124">Nome do pool elástica.</span><span class="sxs-lookup"><span data-stu-id="5de21-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="5de21-125">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5de21-125">EXAMPLES</span></span>

### <span data-ttu-id="5de21-126">Exemplo 1: obter recomendações para um servidor</span><span class="sxs-lookup"><span data-stu-id="5de21-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="5de21-127">Este comando obtém as recomendações de pool elástica para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="5de21-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="5de21-128">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5de21-128">PARAMETERS</span></span>

### <span data-ttu-id="5de21-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de21-129">-DefaultProfile</span></span>
<span data-ttu-id="5de21-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5de21-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5de21-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5de21-131">-ResourceGroupName</span></span>
<span data-ttu-id="5de21-132">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="5de21-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5de21-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5de21-133">-ServerName</span></span>
<span data-ttu-id="5de21-134">Especifica o nome do servidor para o qual este cmdlet obtém recomendações.</span><span class="sxs-lookup"><span data-stu-id="5de21-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="5de21-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5de21-135">-Confirm</span></span>
<span data-ttu-id="5de21-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5de21-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5de21-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5de21-137">-WhatIf</span></span>
<span data-ttu-id="5de21-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5de21-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5de21-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5de21-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5de21-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de21-140">CommonParameters</span></span>
<span data-ttu-id="5de21-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5de21-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de21-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5de21-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de21-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5de21-143">INPUTS</span></span>

### <span data-ttu-id="5de21-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5de21-144">System.String</span></span>

## <span data-ttu-id="5de21-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5de21-145">OUTPUTS</span></span>

### <span data-ttu-id="5de21-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="5de21-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="5de21-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="5de21-147">NOTES</span></span>

## <span data-ttu-id="5de21-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5de21-148">RELATED LINKS</span></span>
