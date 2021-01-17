---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427650"
---
# <span data-ttu-id="ae2f2-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae2f2-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="ae2f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2f2-103">Esse comando excluirá o ponto de extremidade do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="ae2f2-104">A sincronização com este local será interrompida imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="ae2f2-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae2f2-105">SYNTAX</span></span>

### <span data-ttu-id="ae2f2-106">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae2f2-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2f2-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae2f2-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2f2-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae2f2-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae2f2-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae2f2-109">DESCRIPTION</span></span>
<span data-ttu-id="ae2f2-110">A remoção de um ponto de extremidade do servidor é uma operação destrutiva.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="ae2f2-111">Este local de servidor irá parar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-111">This server location will stop syncing.</span></span> <span data-ttu-id="ae2f2-112">Esta operação não deve ser realizada para solucionar problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="ae2f2-113">Se esse local do servidor (incl. is Files) for adicionado novamente ao mesmo grupo de sincronização que um ponto de extremidade do servidor, ele pode levar a arquivos conflitantes e outras conseqüências indesejadas.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="ae2f2-114">Este comando destina-se somente a descomissionamento.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="ae2f2-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae2f2-115">EXAMPLES</span></span>

### <span data-ttu-id="ae2f2-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae2f2-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="ae2f2-117">Esse comando irá remover o ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="ae2f2-118">OS</span><span class="sxs-lookup"><span data-stu-id="ae2f2-118">PARAMETERS</span></span>

### <span data-ttu-id="ae2f2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae2f2-119">-AsJob</span></span>
<span data-ttu-id="ae2f2-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ae2f2-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae2f2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2f2-121">-DefaultProfile</span></span>
<span data-ttu-id="ae2f2-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae2f2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ae2f2-123">-Force</span></span>
<span data-ttu-id="ae2f2-124">Supply-Force para ignorar a confirmação desse comando.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="ae2f2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae2f2-125">-InputObject</span></span>
<span data-ttu-id="ae2f2-126">Objeto de entrada ServerEndpoint, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2f2-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae2f2-127">-Name</span></span>
<span data-ttu-id="ae2f2-128">Nome do ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-128">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2f2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae2f2-129">-PassThru</span></span>
<span data-ttu-id="ae2f2-130">Na execução normal, esse cmdlet retorna nenhum valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="ae2f2-131">Se você fornecer o parâmetro PassThru, o cmdlet irá escrever um valor para o pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="ae2f2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2f2-132">-ResourceGroupName</span></span>
<span data-ttu-id="ae2f2-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="ae2f2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae2f2-134">-ResourceId</span></span>
<span data-ttu-id="ae2f2-135">ID do recurso ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae2f2-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="ae2f2-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ae2f2-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="ae2f2-137">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-137">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2f2-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2f2-138">-SyncGroupName</span></span>
<span data-ttu-id="ae2f2-139">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-139">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2f2-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae2f2-140">-Confirm</span></span>
<span data-ttu-id="ae2f2-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae2f2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae2f2-142">-WhatIf</span></span>
<span data-ttu-id="ae2f2-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae2f2-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae2f2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2f2-145">CommonParameters</span></span>
<span data-ttu-id="ae2f2-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2f2-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae2f2-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2f2-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae2f2-148">INPUTS</span></span>

### <span data-ttu-id="ae2f2-149">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae2f2-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="ae2f2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ae2f2-150">System.String</span></span>

## <span data-ttu-id="ae2f2-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae2f2-151">OUTPUTS</span></span>

### <span data-ttu-id="ae2f2-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="ae2f2-152">System.Object</span></span>
## <span data-ttu-id="ae2f2-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae2f2-153">NOTES</span></span>

## <span data-ttu-id="ae2f2-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae2f2-154">RELATED LINKS</span></span>
