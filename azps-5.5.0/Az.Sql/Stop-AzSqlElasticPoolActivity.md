---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dc1dffd84a95bd9cffac1dbafb5183d56e0b7c52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118597"
---
# <span data-ttu-id="36c44-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="36c44-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="36c44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36c44-102">SYNOPSIS</span></span>
<span data-ttu-id="36c44-103">Cancela a operação de atualização assíncrona em um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="36c44-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="36c44-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36c44-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36c44-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="36c44-105">DESCRIPTION</span></span>
<span data-ttu-id="36c44-106">O cmdlet **Stop-AzSqlElasticPoolActivity** cancela a operação de atualização assíncrona em um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="36c44-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="36c44-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36c44-107">EXAMPLES</span></span>

### <span data-ttu-id="36c44-108">Exemplo 1: Cancelar a operação de atualização assíncrona em um pool elástica</span><span class="sxs-lookup"><span data-stu-id="36c44-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="36c44-109">Esse comando cancela a operação assíncrona de atualizações no pool elástica.</span><span class="sxs-lookup"><span data-stu-id="36c44-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="36c44-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36c44-110">PARAMETERS</span></span>

### <span data-ttu-id="36c44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c44-111">-DefaultProfile</span></span>
<span data-ttu-id="36c44-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36c44-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36c44-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="36c44-113">-ElasticPoolName</span></span>
<span data-ttu-id="36c44-114">O nome do Pool Elástica SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="36c44-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="36c44-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="36c44-115">-OperationId</span></span>
<span data-ttu-id="36c44-116">A ID da operação a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="36c44-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="36c44-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36c44-117">-PassThru</span></span>
<span data-ttu-id="36c44-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="36c44-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c44-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36c44-119">-ResourceGroupName</span></span>
<span data-ttu-id="36c44-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36c44-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="36c44-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36c44-121">-ServerName</span></span>
<span data-ttu-id="36c44-122">O nome do SQL Server do Azure em que o Pool Elástica está.</span><span class="sxs-lookup"><span data-stu-id="36c44-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="36c44-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="36c44-123">-Confirm</span></span>
<span data-ttu-id="36c44-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36c44-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c44-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36c44-125">-WhatIf</span></span>
<span data-ttu-id="36c44-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="36c44-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36c44-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36c44-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c44-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c44-128">CommonParameters</span></span>
<span data-ttu-id="36c44-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36c44-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c44-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36c44-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c44-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="36c44-131">INPUTS</span></span>

### <span data-ttu-id="36c44-132">System.String</span><span class="sxs-lookup"><span data-stu-id="36c44-132">System.String</span></span>

### <span data-ttu-id="36c44-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="36c44-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="36c44-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="36c44-134">OUTPUTS</span></span>

### <span data-ttu-id="36c44-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="36c44-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="36c44-136">Notas</span><span class="sxs-lookup"><span data-stu-id="36c44-136">NOTES</span></span>

## <span data-ttu-id="36c44-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36c44-137">RELATED LINKS</span></span>
