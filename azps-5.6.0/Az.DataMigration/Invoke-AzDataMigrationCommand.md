---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: e99e2e6a8c0b2c8a0fc0b2d2143d2b4301520ab0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885467"
---
# <span data-ttu-id="bfa50-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="bfa50-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="bfa50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfa50-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa50-103">Cria um novo comando a ser executado em uma tarefa DMS existente.</span><span class="sxs-lookup"><span data-stu-id="bfa50-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="bfa50-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bfa50-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="bfa50-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bfa50-105">DESCRIPTION</span></span>
<span data-ttu-id="bfa50-106">O Invoke-AzDataMigrationCommand cmdlet cria uma nova tarefa de comando a ser executado em uma tarefa de migração existente.</span><span class="sxs-lookup"><span data-stu-id="bfa50-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="bfa50-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfa50-107">EXAMPLES</span></span>

### <span data-ttu-id="bfa50-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfa50-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="bfa50-109">Os exemplos acima usam o cmdlet Invoke-AzDataMigrationCommand para criar um comando para um serviço, projeto e tarefa existentes</span><span class="sxs-lookup"><span data-stu-id="bfa50-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="bfa50-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bfa50-110">PARAMETERS</span></span>

### <span data-ttu-id="bfa50-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="bfa50-111">-CommandType</span></span>
<span data-ttu-id="bfa50-112">Tipo de comando.</span><span class="sxs-lookup"><span data-stu-id="bfa50-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa50-113">-DefaultProfile</span></span>
<span data-ttu-id="bfa50-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa50-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa50-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="bfa50-115">-ProjectName</span></span>
<span data-ttu-id="bfa50-116">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="bfa50-116">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa50-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa50-117">-ResourceGroupName</span></span>
<span data-ttu-id="bfa50-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bfa50-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa50-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bfa50-119">-ServiceName</span></span>
<span data-ttu-id="bfa50-120">Nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="bfa50-120">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa50-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="bfa50-121">-TaskName</span></span>
<span data-ttu-id="bfa50-122">O nome da tarefa em que o comando é executado.</span><span class="sxs-lookup"><span data-stu-id="bfa50-122">The name of the task the command is run on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="bfa50-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="bfa50-123">-ObjectName</span></span>
<span data-ttu-id="bfa50-124">O nome do objeto de banco de dados em que o comando será executado.</span><span class="sxs-lookup"><span data-stu-id="bfa50-124">The name of the database object the command will run against.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa50-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfa50-125">-Confirm</span></span>
<span data-ttu-id="bfa50-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa50-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfa50-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfa50-127">-WhatIf</span></span>
<span data-ttu-id="bfa50-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bfa50-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfa50-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfa50-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfa50-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa50-130">CommonParameters</span></span>
<span data-ttu-id="bfa50-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa50-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa50-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfa50-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa50-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfa50-133">INPUTS</span></span>

### <span data-ttu-id="bfa50-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bfa50-134">System.String</span></span>

## <span data-ttu-id="bfa50-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bfa50-135">OUTPUTS</span></span>

### <span data-ttu-id="bfa50-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span><span class="sxs-lookup"><span data-stu-id="bfa50-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="bfa50-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="bfa50-137">NOTES</span></span>

## <span data-ttu-id="bfa50-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfa50-138">RELATED LINKS</span></span>
