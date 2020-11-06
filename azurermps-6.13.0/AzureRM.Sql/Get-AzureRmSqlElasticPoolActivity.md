---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: f5e7455a253c86fe363b72c5d4c0e8ff47b96f56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603426"
---
# <span data-ttu-id="4b500-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="4b500-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="4b500-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b500-102">SYNOPSIS</span></span>
<span data-ttu-id="4b500-103">Obtém o status das operações em um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="4b500-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b500-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b500-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b500-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b500-105">DESCRIPTION</span></span>
<span data-ttu-id="4b500-106">O cmdlet **Get-AzureRmSqlElasticPoolActivity** Obtém o status das operações em um pool elástico para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b500-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="4b500-107">Você pode ver o status da criação e das atualizações de configuração do pool.</span><span class="sxs-lookup"><span data-stu-id="4b500-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="4b500-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b500-108">EXAMPLES</span></span>

### <span data-ttu-id="4b500-109">Exemplo 1: obter o status das operações para um pool elástico</span><span class="sxs-lookup"><span data-stu-id="4b500-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="4b500-110">Esse comando obtém o status das operações do pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="4b500-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="4b500-111">OS</span><span class="sxs-lookup"><span data-stu-id="4b500-111">PARAMETERS</span></span>

### <span data-ttu-id="4b500-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b500-112">-DefaultProfile</span></span>
<span data-ttu-id="4b500-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4b500-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b500-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4b500-114">-ElasticPoolName</span></span>
<span data-ttu-id="4b500-115">Especifica o nome de um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="4b500-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="4b500-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4b500-116">-OperationId</span></span>
<span data-ttu-id="4b500-117">A ID da operação a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="4b500-117">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b500-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b500-118">-ResourceGroupName</span></span>
<span data-ttu-id="4b500-119">Especifica o nome de um grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="4b500-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="4b500-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4b500-120">-ServerName</span></span>
<span data-ttu-id="4b500-121">Especifica o nome de um servidor que contém um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="4b500-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="4b500-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b500-122">-Confirm</span></span>
<span data-ttu-id="4b500-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b500-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b500-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b500-124">-WhatIf</span></span>
<span data-ttu-id="4b500-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b500-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b500-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b500-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b500-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b500-127">CommonParameters</span></span>
<span data-ttu-id="4b500-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b500-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b500-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b500-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b500-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b500-130">INPUTS</span></span>

### <span data-ttu-id="4b500-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4b500-131">System.String</span></span>

### <span data-ttu-id="4b500-132">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4b500-132">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4b500-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b500-133">OUTPUTS</span></span>

### <span data-ttu-id="4b500-134">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="4b500-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="4b500-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b500-135">NOTES</span></span>

## <span data-ttu-id="4b500-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b500-136">RELATED LINKS</span></span>

[<span data-ttu-id="4b500-137">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4b500-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4b500-138">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="4b500-138">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="4b500-139">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4b500-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4b500-140">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4b500-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4b500-141">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4b500-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


