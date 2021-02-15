---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: f6de2bf731bc11a4b0ec8b6c894e6d77569ec9ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112483"
---
# <span data-ttu-id="c9b6c-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="c9b6c-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="c9b6c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b6c-103">Aviso: a não registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="c9b6c-104">Esse comando não fará o registro de um servidor do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="c9b6c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9b6c-105">SYNTAX</span></span>

### <span data-ttu-id="c9b6c-106">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c9b6c-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9b6c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9b6c-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9b6c-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9b6c-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9b6c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9b6c-109">DESCRIPTION</span></span>
<span data-ttu-id="c9b6c-110">Esse comando não registrou um servidor do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="c9b6c-111">Aviso: a não registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="c9b6c-112">Ela só deve ser chamada quando você tem certeza de que nenhum caminho neste servidor deve ser sincronizado mais.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="c9b6c-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9b6c-113">EXAMPLES</span></span>

### <span data-ttu-id="c9b6c-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c9b6c-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="c9b6c-115">Esse comando desosterna o servidor, causando exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="c9b6c-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9b6c-116">PARAMETERS</span></span>

### <span data-ttu-id="c9b6c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9b6c-117">-AsJob</span></span>
<span data-ttu-id="c9b6c-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c9b6c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9b6c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b6c-119">-DefaultProfile</span></span>
<span data-ttu-id="c9b6c-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b6c-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c9b6c-121">-Force</span></span>
<span data-ttu-id="c9b6c-122">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="c9b6c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9b6c-123">-InputObject</span></span>
<span data-ttu-id="c9b6c-124">Objeto de Entrada RegisteredServer, normalmente passou pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c9b6c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9b6c-125">-PassThru</span></span>
<span data-ttu-id="c9b6c-126">Em execução normal, este cmdlet não retorna nenhum valor sobre o sucesso.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="c9b6c-127">Se você fornecer o parâmetro PassThru, o cmdlet gravará um valor no pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="c9b6c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b6c-128">-ResourceGroupName</span></span>
<span data-ttu-id="c9b6c-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="c9b6c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9b6c-130">-ResourceId</span></span>
<span data-ttu-id="c9b6c-131">ID do Recurso RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="c9b6c-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="c9b6c-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="c9b6c-132">-ServerId</span></span>
<span data-ttu-id="c9b6c-133">Nome do RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="c9b6c-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c9b6c-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="c9b6c-135">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c9b6c-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c9b6c-136">-Confirm</span></span>
<span data-ttu-id="c9b6c-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9b6c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b6c-138">-WhatIf</span></span>
<span data-ttu-id="c9b6c-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9b6c-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9b6c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b6c-141">CommonParameters</span></span>
<span data-ttu-id="c9b6c-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b6c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b6c-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9b6c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b6c-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="c9b6c-144">INPUTS</span></span>

### <span data-ttu-id="c9b6c-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="c9b6c-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="c9b6c-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c9b6c-146">System.String</span></span>

### <span data-ttu-id="c9b6c-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c9b6c-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c9b6c-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="c9b6c-148">OUTPUTS</span></span>

### <span data-ttu-id="c9b6c-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="c9b6c-149">System.Object</span></span>
## <span data-ttu-id="c9b6c-150">Notas</span><span class="sxs-lookup"><span data-stu-id="c9b6c-150">NOTES</span></span>

## <span data-ttu-id="c9b6c-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9b6c-151">RELATED LINKS</span></span>
