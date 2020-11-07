---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: f00c1499e7f7e8a5a6d6b14bcbd8289b35ae2ced
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770900"
---
# <span data-ttu-id="adc9f-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="adc9f-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="adc9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adc9f-102">SYNOPSIS</span></span>
<span data-ttu-id="adc9f-103">Cria um novo comando para ser executado em uma tarefa DMS existente.</span><span class="sxs-lookup"><span data-stu-id="adc9f-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="adc9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adc9f-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="adc9f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adc9f-105">DESCRIPTION</span></span>
<span data-ttu-id="adc9f-106">O cmdlet Invoke-AzDataMigrationCommand cria uma nova tarefa de comando para ser executada em uma tarefa de migração existente.</span><span class="sxs-lookup"><span data-stu-id="adc9f-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="adc9f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adc9f-107">EXAMPLES</span></span>

### <span data-ttu-id="adc9f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="adc9f-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="adc9f-109">Os exemplos acima usam o cmdlet Invoke-AzDataMigrationCommand para criar um comando para um serviço, projeto e tarefa existentes</span><span class="sxs-lookup"><span data-stu-id="adc9f-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="adc9f-110">OS</span><span class="sxs-lookup"><span data-stu-id="adc9f-110">PARAMETERS</span></span>

### <span data-ttu-id="adc9f-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="adc9f-111">-CommandType</span></span>
<span data-ttu-id="adc9f-112">Tipo de comando.</span><span class="sxs-lookup"><span data-stu-id="adc9f-112">Command Type.</span></span>

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

### <span data-ttu-id="adc9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc9f-113">-DefaultProfile</span></span>
<span data-ttu-id="adc9f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="adc9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adc9f-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="adc9f-115">-ProjectName</span></span>
<span data-ttu-id="adc9f-116">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="adc9f-116">The name of the project.</span></span>

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

### <span data-ttu-id="adc9f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc9f-117">-ResourceGroupName</span></span>
<span data-ttu-id="adc9f-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="adc9f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="adc9f-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="adc9f-119">-ServiceName</span></span>
<span data-ttu-id="adc9f-120">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="adc9f-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="adc9f-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="adc9f-121">-TaskName</span></span>
<span data-ttu-id="adc9f-122">O nome da tarefa na qual o comando é executado.</span><span class="sxs-lookup"><span data-stu-id="adc9f-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="adc9f-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="adc9f-123">-ObjectName</span></span>
<span data-ttu-id="adc9f-124">O nome do objeto de banco de dados no qual o comando será executado.</span><span class="sxs-lookup"><span data-stu-id="adc9f-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="adc9f-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="adc9f-125">-Confirm</span></span>
<span data-ttu-id="adc9f-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adc9f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adc9f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc9f-127">-WhatIf</span></span>
<span data-ttu-id="adc9f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="adc9f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adc9f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="adc9f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adc9f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc9f-130">CommonParameters</span></span>
<span data-ttu-id="adc9f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc9f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc9f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adc9f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc9f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adc9f-133">INPUTS</span></span>

### <span data-ttu-id="adc9f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="adc9f-134">System.String</span></span>

## <span data-ttu-id="adc9f-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adc9f-135">OUTPUTS</span></span>

### <span data-ttu-id="adc9f-136">Microsoft. Azure. Management. datamigration. Models. Commandproperties</span><span class="sxs-lookup"><span data-stu-id="adc9f-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="adc9f-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adc9f-137">NOTES</span></span>

## <span data-ttu-id="adc9f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adc9f-138">RELATED LINKS</span></span>
