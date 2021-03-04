---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 013a7c40a5acfb4306d53e0ff5b8da1b54f86e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891597"
---
# <span data-ttu-id="ab553-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ab553-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="ab553-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab553-102">SYNOPSIS</span></span>
<span data-ttu-id="ab553-103">Obtém o status das operações em um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="ab553-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="ab553-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ab553-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab553-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ab553-105">DESCRIPTION</span></span>
<span data-ttu-id="ab553-106">O cmdlet **Get-AzSqlElasticPoolActivity** obtém o status das operações em um pool elástica para um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ab553-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="ab553-107">Você pode ver o status das atualizações de configuração e criação de pool.</span><span class="sxs-lookup"><span data-stu-id="ab553-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="ab553-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab553-108">EXAMPLES</span></span>

### <span data-ttu-id="ab553-109">Exemplo 1: Obter o status das operações para um pool elástica</span><span class="sxs-lookup"><span data-stu-id="ab553-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ab553-110">Este comando obtém o status das operações do pool elástica chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="ab553-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="ab553-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ab553-111">PARAMETERS</span></span>

### <span data-ttu-id="ab553-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab553-112">-DefaultProfile</span></span>
<span data-ttu-id="ab553-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ab553-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab553-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ab553-114">-ElasticPoolName</span></span>
<span data-ttu-id="ab553-115">Especifica o nome de um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="ab553-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="ab553-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ab553-116">-OperationId</span></span>
<span data-ttu-id="ab553-117">A ID da operação a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="ab553-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="ab553-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab553-118">-ResourceGroupName</span></span>
<span data-ttu-id="ab553-119">Especifica o nome de um grupo de recursos ao qual o pool elástica é atribuído.</span><span class="sxs-lookup"><span data-stu-id="ab553-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="ab553-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ab553-120">-ServerName</span></span>
<span data-ttu-id="ab553-121">Especifica o nome de um servidor que contém um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="ab553-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="ab553-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab553-122">-Confirm</span></span>
<span data-ttu-id="ab553-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab553-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab553-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab553-124">-WhatIf</span></span>
<span data-ttu-id="ab553-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab553-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab553-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab553-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab553-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab553-127">CommonParameters</span></span>
<span data-ttu-id="ab553-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab553-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab553-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab553-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab553-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab553-130">INPUTS</span></span>

### <span data-ttu-id="ab553-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ab553-131">System.String</span></span>

### <span data-ttu-id="ab553-132">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ab553-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ab553-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ab553-133">OUTPUTS</span></span>

### <span data-ttu-id="ab553-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="ab553-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="ab553-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="ab553-135">NOTES</span></span>

## <span data-ttu-id="ab553-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab553-136">RELATED LINKS</span></span>

[<span data-ttu-id="ab553-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ab553-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="ab553-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ab553-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="ab553-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ab553-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="ab553-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ab553-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="ab553-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ab553-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


