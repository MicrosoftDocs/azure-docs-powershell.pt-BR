---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113741"
---
# <span data-ttu-id="6af7f-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="6af7f-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="6af7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6af7f-102">SYNOPSIS</span></span>
<span data-ttu-id="6af7f-103">Recebe recomendações de pool elásticas.</span><span class="sxs-lookup"><span data-stu-id="6af7f-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="6af7f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6af7f-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6af7f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6af7f-105">DESCRIPTION</span></span>
<span data-ttu-id="6af7f-106">O cmdlet **Get-AzSqlElasticPoolRecommendation** recebe recomendações de pool elásticas para um servidor.</span><span class="sxs-lookup"><span data-stu-id="6af7f-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="6af7f-107">Estas recomendações incluem os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6af7f-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="6af7f-108">Databasecollection.</span><span class="sxs-lookup"><span data-stu-id="6af7f-108">DatabaseCollection.</span></span> <span data-ttu-id="6af7f-109">Conjunto de nomes de banco de dados que pertencem ao pool.</span><span class="sxs-lookup"><span data-stu-id="6af7f-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="6af7f-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="6af7f-110">DatabaseDtuMin.</span></span> <span data-ttu-id="6af7f-111">Garantia de DTU (Unidade de Transmissão de Dados) para bancos de dados no pool elástica.</span><span class="sxs-lookup"><span data-stu-id="6af7f-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="6af7f-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="6af7f-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="6af7f-113">DTU cap para bancos de dados no pool elástica.</span><span class="sxs-lookup"><span data-stu-id="6af7f-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="6af7f-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="6af7f-114">Dtu.</span></span> <span data-ttu-id="6af7f-115">Garantia DTU para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="6af7f-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="6af7f-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="6af7f-116">StorageMb.</span></span> <span data-ttu-id="6af7f-117">Armazenamento em megabytes para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="6af7f-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="6af7f-118">Edição.</span><span class="sxs-lookup"><span data-stu-id="6af7f-118">Edition.</span></span> <span data-ttu-id="6af7f-119">Edição para o pool de elástica.</span><span class="sxs-lookup"><span data-stu-id="6af7f-119">Edition for the elastic pool.</span></span> <span data-ttu-id="6af7f-120">Os valores aceitáveis para este parâmetro são: Básico, Padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="6af7f-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="6af7f-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="6af7f-121">IncludeAllDatabases.</span></span> <span data-ttu-id="6af7f-122">Indica se todos os bancos de dados no pool elástica são retornados.</span><span class="sxs-lookup"><span data-stu-id="6af7f-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="6af7f-123">Nome.</span><span class="sxs-lookup"><span data-stu-id="6af7f-123">Name.</span></span> <span data-ttu-id="6af7f-124">Nome do pool elástica.</span><span class="sxs-lookup"><span data-stu-id="6af7f-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="6af7f-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6af7f-125">EXAMPLES</span></span>

### <span data-ttu-id="6af7f-126">Exemplo 1: Obter recomendações para um servidor</span><span class="sxs-lookup"><span data-stu-id="6af7f-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="6af7f-127">Esse comando obtém as recomendações de pool elásticas para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="6af7f-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="6af7f-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6af7f-128">PARAMETERS</span></span>

### <span data-ttu-id="6af7f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af7f-129">-DefaultProfile</span></span>
<span data-ttu-id="6af7f-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6af7f-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6af7f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6af7f-131">-ResourceGroupName</span></span>
<span data-ttu-id="6af7f-132">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="6af7f-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6af7f-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6af7f-133">-ServerName</span></span>
<span data-ttu-id="6af7f-134">Especifica o nome do servidor para o qual este cmdlet recebe recomendações.</span><span class="sxs-lookup"><span data-stu-id="6af7f-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="6af7f-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6af7f-135">-Confirm</span></span>
<span data-ttu-id="6af7f-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6af7f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6af7f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6af7f-137">-WhatIf</span></span>
<span data-ttu-id="6af7f-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6af7f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6af7f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6af7f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6af7f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af7f-140">CommonParameters</span></span>
<span data-ttu-id="6af7f-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6af7f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af7f-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6af7f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af7f-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="6af7f-143">INPUTS</span></span>

### <span data-ttu-id="6af7f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6af7f-144">System.String</span></span>

## <span data-ttu-id="6af7f-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="6af7f-145">OUTPUTS</span></span>

### <span data-ttu-id="6af7f-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="6af7f-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="6af7f-147">Notas</span><span class="sxs-lookup"><span data-stu-id="6af7f-147">NOTES</span></span>

## <span data-ttu-id="6af7f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6af7f-148">RELATED LINKS</span></span>
