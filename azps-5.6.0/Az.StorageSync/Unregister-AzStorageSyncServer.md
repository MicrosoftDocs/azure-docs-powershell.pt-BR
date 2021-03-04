---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 5ebcdee62997ed678b9696264a40076a40c36342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888133"
---
# <span data-ttu-id="e2b3e-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="e2b3e-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="e2b3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b3e-103">Aviso: o não registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="e2b3e-104">Esse comando desacreva um servidor do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="e2b3e-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e2b3e-105">SYNTAX</span></span>

### <span data-ttu-id="e2b3e-106">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e2b3e-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2b3e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b3e-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2b3e-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b3e-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2b3e-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e2b3e-109">DESCRIPTION</span></span>
<span data-ttu-id="e2b3e-110">Esse comando desacreva um servidor do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="e2b3e-111">Aviso: o não registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="e2b3e-112">Ele só deve ser chamado quando você estiver certo de que nenhum caminho neste servidor deve ser sincronizado mais.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="e2b3e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2b3e-113">EXAMPLES</span></span>

### <span data-ttu-id="e2b3e-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e2b3e-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="e2b3e-115">Esse comando desatará o registro do servidor, causando exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="e2b3e-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e2b3e-116">PARAMETERS</span></span>

### <span data-ttu-id="e2b3e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2b3e-117">-AsJob</span></span>
<span data-ttu-id="e2b3e-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e2b3e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2b3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b3e-119">-DefaultProfile</span></span>
<span data-ttu-id="e2b3e-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b3e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e2b3e-121">-Force</span></span>
<span data-ttu-id="e2b3e-122">Supply -Force para ignorar a confirmação deste comando.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-122">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b3e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2b3e-123">-InputObject</span></span>
<span data-ttu-id="e2b3e-124">Objeto de Entrada RegisteredServer, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b3e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2b3e-125">-PassThru</span></span>
<span data-ttu-id="e2b3e-126">Em execução normal, esse cmdlet não retorna nenhum valor sobre o sucesso.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="e2b3e-127">Se você fornecer o parâmetro PassThru, o cmdlet gravará um valor no pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="e2b3e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b3e-128">-ResourceGroupName</span></span>
<span data-ttu-id="e2b3e-129">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b3e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2b3e-130">-ResourceId</span></span>
<span data-ttu-id="e2b3e-131">ID do Recurso RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="e2b3e-131">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b3e-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="e2b3e-132">-ServerId</span></span>
<span data-ttu-id="e2b3e-133">Nome do RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-133">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b3e-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e2b3e-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="e2b3e-135">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-135">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b3e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2b3e-136">-Confirm</span></span>
<span data-ttu-id="e2b3e-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2b3e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b3e-138">-WhatIf</span></span>
<span data-ttu-id="e2b3e-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2b3e-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2b3e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b3e-141">CommonParameters</span></span>
<span data-ttu-id="e2b3e-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b3e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b3e-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2b3e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b3e-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2b3e-144">INPUTS</span></span>

### <span data-ttu-id="e2b3e-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="e2b3e-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="e2b3e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e2b3e-146">System.String</span></span>

### <span data-ttu-id="e2b3e-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e2b3e-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e2b3e-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e2b3e-148">OUTPUTS</span></span>

### <span data-ttu-id="e2b3e-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="e2b3e-149">System.Object</span></span>
## <span data-ttu-id="e2b3e-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="e2b3e-150">NOTES</span></span>

## <span data-ttu-id="e2b3e-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2b3e-151">RELATED LINKS</span></span>
