---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 999fd83af11422f1499e386f194fd75d9b99e152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429283"
---
# <span data-ttu-id="7e8f8-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="7e8f8-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="7e8f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8f8-103">Cancela a operação de atualização assíncrona em um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e8f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e8f8-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e8f8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e8f8-105">DESCRIPTION</span></span>
<span data-ttu-id="7e8f8-106">O cmdlet **Stop-AzureRmSqlElasticPoolActivity** cancela a operação de atualização assíncrona em um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="7e8f8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e8f8-107">EXAMPLES</span></span>

### <span data-ttu-id="7e8f8-108">Exemplo 1: cancelar a operação de atualização assíncrona em um pool elástico</span><span class="sxs-lookup"><span data-stu-id="7e8f8-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="7e8f8-109">Esse comando cancela a operação de atualizações assíncronas no pool elástico.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="7e8f8-110">OS</span><span class="sxs-lookup"><span data-stu-id="7e8f8-110">PARAMETERS</span></span>

### <span data-ttu-id="7e8f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8f8-111">-DefaultProfile</span></span>
<span data-ttu-id="7e8f8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e8f8-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7e8f8-113">-ElasticPoolName</span></span>
<span data-ttu-id="7e8f8-114">O nome do pool elástico do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="7e8f8-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7e8f8-115">-OperationId</span></span>
<span data-ttu-id="7e8f8-116">A ID da operação a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="7e8f8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e8f8-117">-PassThru</span></span>
<span data-ttu-id="7e8f8-118">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="7e8f8-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7e8f8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e8f8-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e8f8-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e8f8-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="7e8f8-121">-ServerName</span></span>
<span data-ttu-id="7e8f8-122">O nome do Azure SQL Server no qual o pool elástico está.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="7e8f8-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e8f8-123">-Confirm</span></span>
<span data-ttu-id="7e8f8-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e8f8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e8f8-125">-WhatIf</span></span>
<span data-ttu-id="7e8f8-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e8f8-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e8f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8f8-128">CommonParameters</span></span>
<span data-ttu-id="7e8f8-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8f8-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e8f8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8f8-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e8f8-131">INPUTS</span></span>

### <span data-ttu-id="7e8f8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7e8f8-132">System.String</span></span>

### <span data-ttu-id="7e8f8-133">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7e8f8-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7e8f8-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e8f8-134">OUTPUTS</span></span>

### <span data-ttu-id="7e8f8-135">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="7e8f8-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="7e8f8-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e8f8-136">NOTES</span></span>

## <span data-ttu-id="7e8f8-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e8f8-137">RELATED LINKS</span></span>
