---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Invoke-AzureRmDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
ms.openlocfilehash: 882d7eb0b005478850addda2d066c7266e6c2ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431970"
---
# <span data-ttu-id="0cd70-101">Invoke-AzureRmDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="0cd70-101">Invoke-AzureRmDataMigrationCommand</span></span>

## <span data-ttu-id="0cd70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cd70-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd70-103">Cria um novo comando para ser executado em uma tarefa DMS existente.</span><span class="sxs-lookup"><span data-stu-id="0cd70-103">Creates a new command to be executed on an existing DMS task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cd70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cd70-104">SYNTAX</span></span>

```
Invoke-AzureRmDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cd70-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0cd70-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd70-106">O cmdlet New-AzureRmDataMigrationCommand cria uma nova tarefa de comando para ser executada em uma tarefa de migração existente.</span><span class="sxs-lookup"><span data-stu-id="0cd70-106">The New-AzureRmDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="0cd70-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0cd70-107">EXAMPLES</span></span>

### <span data-ttu-id="0cd70-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0cd70-108">Example 1</span></span>
```
PS C:\> $command = New-AzureRmDmsCommand -CommandType Complete -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="0cd70-109">Os exemplos acima usam o cmdlet New-AzureRmDmsCommand para criar um comando para um serviço, projeto e tarefa existentes</span><span class="sxs-lookup"><span data-stu-id="0cd70-109">The above examples uses the New-AzureRmDmsCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="0cd70-110">OS</span><span class="sxs-lookup"><span data-stu-id="0cd70-110">PARAMETERS</span></span>

### <span data-ttu-id="0cd70-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="0cd70-111">-CommandType</span></span>
<span data-ttu-id="0cd70-112">Tipo de comando.</span><span class="sxs-lookup"><span data-stu-id="0cd70-112">Command Type.</span></span>

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

### <span data-ttu-id="0cd70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd70-113">-DefaultProfile</span></span>
<span data-ttu-id="0cd70-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0cd70-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cd70-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="0cd70-115">-ProjectName</span></span>
<span data-ttu-id="0cd70-116">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="0cd70-116">The name of the project.</span></span>

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

### <span data-ttu-id="0cd70-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cd70-117">-ResourceGroupName</span></span>
<span data-ttu-id="0cd70-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0cd70-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="0cd70-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0cd70-119">-ServiceName</span></span>
<span data-ttu-id="0cd70-120">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0cd70-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="0cd70-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="0cd70-121">-TaskName</span></span>
<span data-ttu-id="0cd70-122">O nome da tarefa na qual o comando é executado.</span><span class="sxs-lookup"><span data-stu-id="0cd70-122">The name of the task the command is run on.</span></span>

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

### <span data-ttu-id="0cd70-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0cd70-123">-Confirm</span></span>
<span data-ttu-id="0cd70-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cd70-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cd70-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cd70-125">-WhatIf</span></span>
<span data-ttu-id="0cd70-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0cd70-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cd70-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0cd70-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cd70-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd70-128">CommonParameters</span></span>
<span data-ttu-id="0cd70-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd70-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd70-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd70-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd70-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0cd70-131">INPUTS</span></span>

### <span data-ttu-id="0cd70-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0cd70-132">System.String</span></span>

## <span data-ttu-id="0cd70-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0cd70-133">OUTPUTS</span></span>

### <span data-ttu-id="0cd70-134">Microsoft. Azure. Management. datamigration. Models. Commandproperties</span><span class="sxs-lookup"><span data-stu-id="0cd70-134">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="0cd70-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0cd70-135">NOTES</span></span>

## <span data-ttu-id="0cd70-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cd70-136">RELATED LINKS</span></span>
