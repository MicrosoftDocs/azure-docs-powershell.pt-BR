---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281575"
---
# <span data-ttu-id="69e62-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="69e62-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="69e62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69e62-102">SYNOPSIS</span></span>
<span data-ttu-id="69e62-103">Cancela o serviço de reprodução de log ao descartar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="69e62-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="69e62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69e62-104">SYNTAX</span></span>

### <span data-ttu-id="69e62-105">LogReplayInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="69e62-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69e62-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="69e62-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69e62-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69e62-107">DESCRIPTION</span></span>
<span data-ttu-id="69e62-108">O cmdlet **Stop-AzSqlInstanceDatabaseLogReplay** descarta o banco de dados e, por isso, cancela o serviço de reprodução de log.</span><span class="sxs-lookup"><span data-stu-id="69e62-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="69e62-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69e62-109">EXAMPLES</span></span>

### <span data-ttu-id="69e62-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69e62-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="69e62-111">Esse comando cancelará o serviço de reprodução de logs no banco de dados fornecido.</span><span class="sxs-lookup"><span data-stu-id="69e62-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="69e62-112">OS</span><span class="sxs-lookup"><span data-stu-id="69e62-112">PARAMETERS</span></span>

### <span data-ttu-id="69e62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e62-113">-DefaultProfile</span></span>
<span data-ttu-id="69e62-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69e62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69e62-115">-Force</span><span class="sxs-lookup"><span data-stu-id="69e62-115">-Force</span></span>
<span data-ttu-id="69e62-116">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="69e62-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="69e62-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69e62-117">-InputObject</span></span>
<span data-ttu-id="69e62-118">O objeto de banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="69e62-118">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69e62-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="69e62-119">-InstanceName</span></span>
<span data-ttu-id="69e62-120">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="69e62-120">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69e62-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="69e62-121">-Name</span></span>
<span data-ttu-id="69e62-122">O nome do banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="69e62-122">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69e62-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69e62-123">-PassThru</span></span>
<span data-ttu-id="69e62-124">Define se retorna o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="69e62-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="69e62-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69e62-125">-ResourceGroupName</span></span>
<span data-ttu-id="69e62-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69e62-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69e62-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69e62-127">-Confirm</span></span>
<span data-ttu-id="69e62-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69e62-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69e62-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69e62-129">-WhatIf</span></span>
<span data-ttu-id="69e62-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69e62-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69e62-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69e62-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69e62-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e62-132">CommonParameters</span></span>
<span data-ttu-id="69e62-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69e62-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e62-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69e62-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e62-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69e62-135">INPUTS</span></span>

### <span data-ttu-id="69e62-136">System. String</span><span class="sxs-lookup"><span data-stu-id="69e62-136">System.String</span></span>

### <span data-ttu-id="69e62-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="69e62-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="69e62-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69e62-138">OUTPUTS</span></span>

### <span data-ttu-id="69e62-139">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="69e62-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="69e62-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69e62-140">NOTES</span></span>

## <span data-ttu-id="69e62-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69e62-141">RELATED LINKS</span></span>
