---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 3752e520c3637ffa1e08bfd89d03c6caeebd4e18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772662"
---
# <span data-ttu-id="77f10-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="77f10-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="77f10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77f10-102">SYNOPSIS</span></span>
<span data-ttu-id="77f10-103">Aviso: o cancelamento do registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="77f10-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="77f10-104">Esse comando cancelará o registro de um servidor do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="77f10-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="77f10-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77f10-105">SYNTAX</span></span>

### <span data-ttu-id="77f10-106">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="77f10-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77f10-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77f10-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77f10-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77f10-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77f10-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77f10-109">DESCRIPTION</span></span>
<span data-ttu-id="77f10-110">Esse comando cancelará o registro de um servidor do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="77f10-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="77f10-111">Aviso: o cancelamento do registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="77f10-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="77f10-112">Ele só deve ser chamado quando você tiver certeza de que nenhum caminho neste servidor será mais sincronizado.</span><span class="sxs-lookup"><span data-stu-id="77f10-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="77f10-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77f10-113">EXAMPLES</span></span>

### <span data-ttu-id="77f10-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="77f10-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="77f10-115">Esse comando cancelará o registro do servidor, causando exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="77f10-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="77f10-116">OS</span><span class="sxs-lookup"><span data-stu-id="77f10-116">PARAMETERS</span></span>

### <span data-ttu-id="77f10-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77f10-117">-AsJob</span></span>
<span data-ttu-id="77f10-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="77f10-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77f10-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f10-119">-DefaultProfile</span></span>
<span data-ttu-id="77f10-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77f10-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77f10-121">-Force</span><span class="sxs-lookup"><span data-stu-id="77f10-121">-Force</span></span>
<span data-ttu-id="77f10-122">Supply-Force para ignorar a confirmação desse comando.</span><span class="sxs-lookup"><span data-stu-id="77f10-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="77f10-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77f10-123">-InputObject</span></span>
<span data-ttu-id="77f10-124">O objeto de entrada RegisteredServer normalmente passou pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="77f10-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="77f10-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77f10-125">-PassThru</span></span>
<span data-ttu-id="77f10-126">Na execução normal, esse cmdlet retorna nenhum valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="77f10-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="77f10-127">Se você fornecer o parâmetro PassThru, o cmdlet irá escrever um valor para o pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="77f10-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="77f10-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f10-128">-ResourceGroupName</span></span>
<span data-ttu-id="77f10-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="77f10-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="77f10-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77f10-130">-ResourceId</span></span>
<span data-ttu-id="77f10-131">ID do recurso de RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="77f10-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="77f10-132">-ServerID</span><span class="sxs-lookup"><span data-stu-id="77f10-132">-ServerId</span></span>
<span data-ttu-id="77f10-133">Nome do RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="77f10-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="77f10-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="77f10-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="77f10-135">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="77f10-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="77f10-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="77f10-136">-Confirm</span></span>
<span data-ttu-id="77f10-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77f10-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77f10-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77f10-138">-WhatIf</span></span>
<span data-ttu-id="77f10-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="77f10-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77f10-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77f10-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77f10-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f10-141">CommonParameters</span></span>
<span data-ttu-id="77f10-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f10-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f10-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77f10-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f10-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77f10-144">INPUTS</span></span>

### <span data-ttu-id="77f10-145">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="77f10-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="77f10-146">System. String</span><span class="sxs-lookup"><span data-stu-id="77f10-146">System.String</span></span>

### <span data-ttu-id="77f10-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="77f10-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="77f10-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77f10-148">OUTPUTS</span></span>

### <span data-ttu-id="77f10-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="77f10-149">System.Object</span></span>
## <span data-ttu-id="77f10-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77f10-150">NOTES</span></span>

## <span data-ttu-id="77f10-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77f10-151">RELATED LINKS</span></span>