---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 41710c328787f542188c828975402696c36f0854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943134"
---
# <span data-ttu-id="7a810-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="7a810-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="7a810-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a810-102">SYNOPSIS</span></span>
<span data-ttu-id="7a810-103">Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces.</span><span class="sxs-lookup"><span data-stu-id="7a810-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="7a810-104">Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7a810-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="7a810-105">No máximo 10.000 itens podem ser detectados.</span><span class="sxs-lookup"><span data-stu-id="7a810-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="7a810-106">Se o escopo das alterações for conhecido, limite a execução desse comando para partes do namespace, para que a detecção de alteração possa terminar rapidamente e dentro do limite de itens do 10.000.</span><span class="sxs-lookup"><span data-stu-id="7a810-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="7a810-107">O cmdlet Invoke-AzStorageSyncChangeDetection não detectará arquivos que foram excluídos no compartilhamento de arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a810-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect files that are deleted in the Azure file share.</span></span> <span data-ttu-id="7a810-108">Se os arquivos forem excluídos do compartilhamento de arquivos do Azure, eles serão detectados quando o [trabalho de detecção de alterações](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) for executado.</span><span class="sxs-lookup"><span data-stu-id="7a810-108">If files are deleted in the Azure file share, they will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="7a810-109">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a810-109">SYNTAX</span></span>

### <span data-ttu-id="7a810-110">StringAndDirectoryParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7a810-110">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a810-111">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a810-111">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a810-112">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a810-112">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a810-113">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a810-113">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a810-114">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a810-114">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a810-115">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a810-115">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a810-116">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a810-116">DESCRIPTION</span></span>
<span data-ttu-id="7a810-117">Periodicamente, a sincronização de arquivos do Azure verifica o namespace dentro de um compartilhamento de arquivos do Azure de sincronização para as alterações que chegavam ao compartilhamento de arquivos por outros meios do que a sincronização. O objetivo é identificar essas alterações e, em última análise, sincronizá-las com os servidores conectados.</span><span class="sxs-lookup"><span data-stu-id="7a810-117">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="7a810-118">Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces.</span><span class="sxs-lookup"><span data-stu-id="7a810-118">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="7a810-119">Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7a810-119">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="7a810-120">Se o escopo das alterações for conhecido, limite a execução desse comando para partes do namespace, para que a detecção de alteração possa terminar rapidamente e dentro de um limite de alterações do 10.000.</span><span class="sxs-lookup"><span data-stu-id="7a810-120">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="7a810-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a810-121">EXAMPLES</span></span>

### <span data-ttu-id="7a810-122">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a810-122">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="7a810-123">Neste exemplo, a detecção de alterações é executada nos diretórios "dados" e "Reporting\Templates" de um compartilhamento de arquivos do Azure em sincronização.</span><span class="sxs-lookup"><span data-stu-id="7a810-123">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="7a810-124">Todos os caminhos são relativos à raiz do namespace do compartilhamento de arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a810-124">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="7a810-125">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7a810-125">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="7a810-126">Neste exemplo, a detecção de alterações é executada para um conjunto de arquivos conhecidos pelo chamador de comando que foram alterados.</span><span class="sxs-lookup"><span data-stu-id="7a810-126">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="7a810-127">O objetivo é fazer com que o Azure File Sync detecte e sincronize essas alterações também.</span><span class="sxs-lookup"><span data-stu-id="7a810-127">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="7a810-128">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7a810-128">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="7a810-129">Neste exemplo, a detecção de alterações é executada para o diretório "exemplos" e detecta recursivamente as alterações em subpastas.</span><span class="sxs-lookup"><span data-stu-id="7a810-129">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="7a810-130">Lembre-se de que esse comando pode detectar até 10.000 alterações antes de ser anulada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7a810-130">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="7a810-131">Se você suspeitar que há mais de 10.000 alterações, execute o comando em subpartes do namespace.</span><span class="sxs-lookup"><span data-stu-id="7a810-131">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="7a810-132">OS</span><span class="sxs-lookup"><span data-stu-id="7a810-132">PARAMETERS</span></span>

### <span data-ttu-id="7a810-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a810-133">-AsJob</span></span>
<span data-ttu-id="7a810-134">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7a810-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a810-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a810-135">-DefaultProfile</span></span>
<span data-ttu-id="7a810-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a810-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a810-137">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="7a810-137">-DirectoryPath</span></span>
<span data-ttu-id="7a810-138">Diretório em que a detecção de alterações será realizada.</span><span class="sxs-lookup"><span data-stu-id="7a810-138">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a810-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a810-139">-InputObject</span></span>
<span data-ttu-id="7a810-140">Objeto CloudEndpoint, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7a810-140">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a810-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a810-141">-Name</span></span>
<span data-ttu-id="7a810-142">Nome do CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7a810-142">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a810-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a810-143">-PassThru</span></span>
<span data-ttu-id="7a810-144">Na execução normal, esse cmdlet retorna nenhum valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="7a810-144">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="7a810-145">Se você fornecer o parâmetro PassThru, o cmdlet irá escrever um valor para o pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7a810-145">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="7a810-146">-Caminho</span><span class="sxs-lookup"><span data-stu-id="7a810-146">-Path</span></span>
<span data-ttu-id="7a810-147">Caminho onde a detecção de alterações será realizada.</span><span class="sxs-lookup"><span data-stu-id="7a810-147">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a810-148">-Recursiva</span><span class="sxs-lookup"><span data-stu-id="7a810-148">-Recursive</span></span>
<span data-ttu-id="7a810-149">Indicação se a detecção de alterações de diretório é recursiva.</span><span class="sxs-lookup"><span data-stu-id="7a810-149">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a810-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a810-150">-ResourceGroupName</span></span>
<span data-ttu-id="7a810-151">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a810-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a810-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a810-152">-ResourceId</span></span>
<span data-ttu-id="7a810-153">ID do recurso CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a810-153">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a810-154">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="7a810-154">-StorageSyncServiceName</span></span>
<span data-ttu-id="7a810-155">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="7a810-155">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a810-156">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7a810-156">-SyncGroupName</span></span>
<span data-ttu-id="7a810-157">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="7a810-157">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a810-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7a810-158">-Confirm</span></span>
<span data-ttu-id="7a810-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a810-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a810-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a810-160">-WhatIf</span></span>
<span data-ttu-id="7a810-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a810-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a810-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a810-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a810-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a810-163">CommonParameters</span></span>
<span data-ttu-id="7a810-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a810-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a810-165">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a810-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a810-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a810-166">INPUTS</span></span>

### <span data-ttu-id="7a810-167">System. String</span><span class="sxs-lookup"><span data-stu-id="7a810-167">System.String</span></span>

### <span data-ttu-id="7a810-168">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a810-168">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="7a810-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a810-169">OUTPUTS</span></span>

### <span data-ttu-id="7a810-170">System. void</span><span class="sxs-lookup"><span data-stu-id="7a810-170">System.Void</span></span>

## <span data-ttu-id="7a810-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a810-171">NOTES</span></span>

## <span data-ttu-id="7a810-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a810-172">RELATED LINKS</span></span>
