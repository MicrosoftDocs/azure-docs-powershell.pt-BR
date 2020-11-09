---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280431"
---
# <span data-ttu-id="0b88a-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="0b88a-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="0b88a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b88a-102">SYNOPSIS</span></span>
<span data-ttu-id="0b88a-103">Obtém recomendações de pool elástico.</span><span class="sxs-lookup"><span data-stu-id="0b88a-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="0b88a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b88a-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b88a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b88a-105">DESCRIPTION</span></span>
<span data-ttu-id="0b88a-106">O cmdlet **Get-AzSqlElasticPoolRecommendation** Obtém recomendações de pool elástico para um servidor.</span><span class="sxs-lookup"><span data-stu-id="0b88a-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="0b88a-107">Essas recomendações incluem os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="0b88a-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="0b88a-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="0b88a-108">DatabaseCollection.</span></span> <span data-ttu-id="0b88a-109">Coleção de nomes de banco de dados que pertencem ao pool.</span><span class="sxs-lookup"><span data-stu-id="0b88a-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="0b88a-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="0b88a-110">DatabaseDtuMin.</span></span> <span data-ttu-id="0b88a-111">A garantia da unidade de transmissão de dados (DTU) para bancos de dados no pool elástico.</span><span class="sxs-lookup"><span data-stu-id="0b88a-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="0b88a-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="0b88a-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="0b88a-113">Cap de DTU para bancos de dados no pool elástico.</span><span class="sxs-lookup"><span data-stu-id="0b88a-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="0b88a-114">DTU.</span><span class="sxs-lookup"><span data-stu-id="0b88a-114">Dtu.</span></span> <span data-ttu-id="0b88a-115">Garantia de DTU para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="0b88a-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="0b88a-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="0b88a-116">StorageMb.</span></span> <span data-ttu-id="0b88a-117">Armazenamento em megabytes para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="0b88a-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="0b88a-118">Edições.</span><span class="sxs-lookup"><span data-stu-id="0b88a-118">Edition.</span></span> <span data-ttu-id="0b88a-119">Edição para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="0b88a-119">Edition for the elastic pool.</span></span> <span data-ttu-id="0b88a-120">Os valores aceitáveis para esse parâmetro são: Basic, Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="0b88a-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="0b88a-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="0b88a-121">IncludeAllDatabases.</span></span> <span data-ttu-id="0b88a-122">Indica se todos os bancos de dados no pool elástico são retornados.</span><span class="sxs-lookup"><span data-stu-id="0b88a-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="0b88a-123">Sobrenome.</span><span class="sxs-lookup"><span data-stu-id="0b88a-123">Name.</span></span> <span data-ttu-id="0b88a-124">Nome do pool elástico.</span><span class="sxs-lookup"><span data-stu-id="0b88a-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="0b88a-125">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b88a-125">EXAMPLES</span></span>

### <span data-ttu-id="0b88a-126">Exemplo 1: obter recomendações para um servidor</span><span class="sxs-lookup"><span data-stu-id="0b88a-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="0b88a-127">Este comando obtém as recomendações de pool elástico para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="0b88a-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="0b88a-128">OS</span><span class="sxs-lookup"><span data-stu-id="0b88a-128">PARAMETERS</span></span>

### <span data-ttu-id="0b88a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b88a-129">-DefaultProfile</span></span>
<span data-ttu-id="0b88a-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0b88a-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b88a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b88a-131">-ResourceGroupName</span></span>
<span data-ttu-id="0b88a-132">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="0b88a-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0b88a-133">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0b88a-133">-ServerName</span></span>
<span data-ttu-id="0b88a-134">Especifica o nome do servidor para o qual este cmdlet obtém recomendações.</span><span class="sxs-lookup"><span data-stu-id="0b88a-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="0b88a-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b88a-135">-Confirm</span></span>
<span data-ttu-id="0b88a-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b88a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b88a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b88a-137">-WhatIf</span></span>
<span data-ttu-id="0b88a-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b88a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b88a-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b88a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b88a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b88a-140">CommonParameters</span></span>
<span data-ttu-id="0b88a-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b88a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b88a-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b88a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b88a-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b88a-143">INPUTS</span></span>

### <span data-ttu-id="0b88a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0b88a-144">System.String</span></span>

## <span data-ttu-id="0b88a-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b88a-145">OUTPUTS</span></span>

### <span data-ttu-id="0b88a-146">Microsoft. Azure. Management. Sql. LegacySdk. Models. UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="0b88a-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="0b88a-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b88a-147">NOTES</span></span>

## <span data-ttu-id="0b88a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b88a-148">RELATED LINKS</span></span>
