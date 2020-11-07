---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 61a72691aaaaf9cbdfd4e0706f6ace17d7291851
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773729"
---
# <span data-ttu-id="64810-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="64810-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="64810-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64810-102">SYNOPSIS</span></span>
<span data-ttu-id="64810-103">Obtém o status das operações em um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="64810-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="64810-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64810-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64810-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64810-105">DESCRIPTION</span></span>
<span data-ttu-id="64810-106">O cmdlet **Get-AzSqlElasticPoolActivity** Obtém o status das operações em um pool elástico para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="64810-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="64810-107">Você pode ver o status da criação e das atualizações de configuração do pool.</span><span class="sxs-lookup"><span data-stu-id="64810-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="64810-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64810-108">EXAMPLES</span></span>

### <span data-ttu-id="64810-109">Exemplo 1: obter o status das operações para um pool elástico</span><span class="sxs-lookup"><span data-stu-id="64810-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="64810-110">Esse comando obtém o status das operações do pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="64810-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="64810-111">OS</span><span class="sxs-lookup"><span data-stu-id="64810-111">PARAMETERS</span></span>

### <span data-ttu-id="64810-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64810-112">-DefaultProfile</span></span>
<span data-ttu-id="64810-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="64810-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64810-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="64810-114">-ElasticPoolName</span></span>
<span data-ttu-id="64810-115">Especifica o nome de um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="64810-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="64810-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="64810-116">-OperationId</span></span>
<span data-ttu-id="64810-117">A ID da operação a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="64810-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="64810-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64810-118">-ResourceGroupName</span></span>
<span data-ttu-id="64810-119">Especifica o nome de um grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="64810-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="64810-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="64810-120">-ServerName</span></span>
<span data-ttu-id="64810-121">Especifica o nome de um servidor que contém um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="64810-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="64810-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64810-122">-Confirm</span></span>
<span data-ttu-id="64810-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64810-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64810-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64810-124">-WhatIf</span></span>
<span data-ttu-id="64810-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64810-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64810-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64810-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64810-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64810-127">CommonParameters</span></span>
<span data-ttu-id="64810-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64810-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64810-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64810-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64810-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64810-130">INPUTS</span></span>

### <span data-ttu-id="64810-131">System. String</span><span class="sxs-lookup"><span data-stu-id="64810-131">System.String</span></span>

### <span data-ttu-id="64810-132">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="64810-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="64810-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64810-133">OUTPUTS</span></span>

### <span data-ttu-id="64810-134">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="64810-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="64810-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64810-135">NOTES</span></span>

## <span data-ttu-id="64810-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64810-136">RELATED LINKS</span></span>

[<span data-ttu-id="64810-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="64810-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="64810-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="64810-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="64810-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="64810-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="64810-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="64810-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="64810-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="64810-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


