---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 88052c9f47359e0080e193f5a2dbb1004b48b0e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602832"
---
# <span data-ttu-id="0efca-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0efca-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="0efca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0efca-102">SYNOPSIS</span></span>
<span data-ttu-id="0efca-103">Obtém o status das operações em um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="0efca-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0efca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0efca-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0efca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0efca-105">DESCRIPTION</span></span>
<span data-ttu-id="0efca-106">O cmdlet **Get-AzureRmSqlElasticPoolActivity** Obtém o status das operações em um pool elástico para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0efca-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="0efca-107">Você pode ver o status da criação e das atualizações de configuração do pool.</span><span class="sxs-lookup"><span data-stu-id="0efca-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="0efca-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0efca-108">EXAMPLES</span></span>

### <span data-ttu-id="0efca-109">Exemplo 1: obter o status das operações para um pool elástico</span><span class="sxs-lookup"><span data-stu-id="0efca-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="0efca-110">Esse comando obtém o status das operações do pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="0efca-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="0efca-111">OS</span><span class="sxs-lookup"><span data-stu-id="0efca-111">PARAMETERS</span></span>

### <span data-ttu-id="0efca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efca-112">-DefaultProfile</span></span>
<span data-ttu-id="0efca-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0efca-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0efca-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0efca-114">-ElasticPoolName</span></span>
<span data-ttu-id="0efca-115">Especifica o nome de um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="0efca-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="0efca-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0efca-116">-ResourceGroupName</span></span>
<span data-ttu-id="0efca-117">Especifica o nome de um grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="0efca-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="0efca-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0efca-118">-ServerName</span></span>
<span data-ttu-id="0efca-119">Especifica o nome de um servidor que contém um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="0efca-119">Specifies the name of a server that contains an elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0efca-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0efca-120">-Confirm</span></span>
<span data-ttu-id="0efca-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0efca-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0efca-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0efca-122">-WhatIf</span></span>
<span data-ttu-id="0efca-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0efca-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0efca-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0efca-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0efca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efca-125">CommonParameters</span></span>
<span data-ttu-id="0efca-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efca-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0efca-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efca-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0efca-128">INPUTS</span></span>

### <span data-ttu-id="0efca-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0efca-129">None</span></span>
<span data-ttu-id="0efca-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0efca-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0efca-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0efca-131">OUTPUTS</span></span>

### <span data-ttu-id="0efca-132">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="0efca-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="0efca-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0efca-133">NOTES</span></span>

## <span data-ttu-id="0efca-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0efca-134">RELATED LINKS</span></span>

[<span data-ttu-id="0efca-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0efca-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="0efca-136">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="0efca-136">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="0efca-137">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0efca-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="0efca-138">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0efca-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="0efca-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0efca-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


