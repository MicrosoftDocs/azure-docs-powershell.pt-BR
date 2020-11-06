---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 47d56a0c15cc3ecf9656ae6c14600adf6a1e2cf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429040"
---
# <span data-ttu-id="fe287-101">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="fe287-101">Get-AzureRmSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="fe287-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe287-102">SYNOPSIS</span></span>
<span data-ttu-id="fe287-103">Obtém recomendações de pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe287-103">Gets elastic pool recommendations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe287-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe287-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe287-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe287-105">DESCRIPTION</span></span>
<span data-ttu-id="fe287-106">O cmdlet **Get-AzureRmSqlElasticPoolRecommendation** Obtém recomendações de pool elástico para um servidor.</span><span class="sxs-lookup"><span data-stu-id="fe287-106">The **Get-AzureRmSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="fe287-107">Essas recomendações incluem os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fe287-107">These recommendations include the following values:</span></span>

- <span data-ttu-id="fe287-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="fe287-108">DatabaseCollection.</span></span> <span data-ttu-id="fe287-109">Coleção de nomes de banco de dados que pertencem ao pool.</span><span class="sxs-lookup"><span data-stu-id="fe287-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="fe287-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="fe287-110">DatabaseDtuMin.</span></span> <span data-ttu-id="fe287-111">A garantia da unidade de transmissão de dados (DTU) para bancos de dados no pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe287-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="fe287-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="fe287-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="fe287-113">Cap de DTU para bancos de dados no pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe287-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="fe287-114">DTU.</span><span class="sxs-lookup"><span data-stu-id="fe287-114">Dtu.</span></span> <span data-ttu-id="fe287-115">Garantia de DTU para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe287-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="fe287-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="fe287-116">StorageMb.</span></span> <span data-ttu-id="fe287-117">Armazenamento em megabytes para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe287-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="fe287-118">Edições.</span><span class="sxs-lookup"><span data-stu-id="fe287-118">Edition.</span></span> <span data-ttu-id="fe287-119">Edição para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe287-119">Edition for the elastic pool.</span></span> <span data-ttu-id="fe287-120">Os valores aceitáveis para esse parâmetro são: Basic, Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="fe287-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="fe287-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="fe287-121">IncludeAllDatabases.</span></span> <span data-ttu-id="fe287-122">Indica se todos os bancos de dados no pool elástico são retornados.</span><span class="sxs-lookup"><span data-stu-id="fe287-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="fe287-123">Sobrenome.</span><span class="sxs-lookup"><span data-stu-id="fe287-123">Name.</span></span> <span data-ttu-id="fe287-124">Nome do pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe287-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="fe287-125">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe287-125">EXAMPLES</span></span>

### <span data-ttu-id="fe287-126">Exemplo 1: obter recomendações para um servidor</span><span class="sxs-lookup"><span data-stu-id="fe287-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="fe287-127">Este comando obtém as recomendações de pool elástico para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="fe287-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="fe287-128">OS</span><span class="sxs-lookup"><span data-stu-id="fe287-128">PARAMETERS</span></span>

### <span data-ttu-id="fe287-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe287-129">-ResourceGroupName</span></span>
<span data-ttu-id="fe287-130">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fe287-130">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fe287-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="fe287-131">-ServerName</span></span>
<span data-ttu-id="fe287-132">Especifica o nome do servidor para o qual este cmdlet obtém recomendações.</span><span class="sxs-lookup"><span data-stu-id="fe287-132">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="fe287-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe287-133">-Confirm</span></span>
<span data-ttu-id="fe287-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe287-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe287-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe287-135">-WhatIf</span></span>
<span data-ttu-id="fe287-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe287-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe287-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe287-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe287-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe287-138">-DefaultProfile</span></span>
<span data-ttu-id="fe287-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe287-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe287-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe287-140">CommonParameters</span></span>
<span data-ttu-id="fe287-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe287-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe287-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe287-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe287-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe287-143">INPUTS</span></span>

## <span data-ttu-id="fe287-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe287-144">OUTPUTS</span></span>

## <span data-ttu-id="fe287-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe287-145">NOTES</span></span>

## <span data-ttu-id="fe287-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe287-146">RELATED LINKS</span></span>

