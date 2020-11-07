---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954625"
---
# <span data-ttu-id="2f55b-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2f55b-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="2f55b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f55b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f55b-103">Obtém o status das operações em um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="2f55b-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="2f55b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f55b-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f55b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f55b-105">DESCRIPTION</span></span>
<span data-ttu-id="2f55b-106">O cmdlet **Get-AzSqlElasticPoolActivity** Obtém o status das operações em um pool elástico para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f55b-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="2f55b-107">Você pode ver o status da criação e das atualizações de configuração do pool.</span><span class="sxs-lookup"><span data-stu-id="2f55b-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="2f55b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f55b-108">EXAMPLES</span></span>

### <span data-ttu-id="2f55b-109">Exemplo 1: obter o status das operações para um pool elástico</span><span class="sxs-lookup"><span data-stu-id="2f55b-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="2f55b-110">Esse comando obtém o status das operações do pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="2f55b-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="2f55b-111">OS</span><span class="sxs-lookup"><span data-stu-id="2f55b-111">PARAMETERS</span></span>

### <span data-ttu-id="2f55b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f55b-112">-DefaultProfile</span></span>
<span data-ttu-id="2f55b-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2f55b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f55b-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2f55b-114">-ElasticPoolName</span></span>
<span data-ttu-id="2f55b-115">Especifica o nome de um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="2f55b-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="2f55b-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2f55b-116">-OperationId</span></span>
<span data-ttu-id="2f55b-117">A ID da operação a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="2f55b-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="2f55b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f55b-118">-ResourceGroupName</span></span>
<span data-ttu-id="2f55b-119">Especifica o nome de um grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="2f55b-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="2f55b-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2f55b-120">-ServerName</span></span>
<span data-ttu-id="2f55b-121">Especifica o nome de um servidor que contém um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="2f55b-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="2f55b-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2f55b-122">-Confirm</span></span>
<span data-ttu-id="2f55b-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f55b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f55b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f55b-124">-WhatIf</span></span>
<span data-ttu-id="2f55b-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f55b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f55b-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f55b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f55b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f55b-127">CommonParameters</span></span>
<span data-ttu-id="2f55b-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f55b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f55b-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f55b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f55b-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f55b-130">INPUTS</span></span>

### <span data-ttu-id="2f55b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2f55b-131">System.String</span></span>

### <span data-ttu-id="2f55b-132">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2f55b-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2f55b-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f55b-133">OUTPUTS</span></span>

### <span data-ttu-id="2f55b-134">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="2f55b-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="2f55b-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f55b-135">NOTES</span></span>

## <span data-ttu-id="2f55b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f55b-136">RELATED LINKS</span></span>

[<span data-ttu-id="2f55b-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2f55b-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="2f55b-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="2f55b-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="2f55b-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2f55b-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="2f55b-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2f55b-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="2f55b-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2f55b-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


