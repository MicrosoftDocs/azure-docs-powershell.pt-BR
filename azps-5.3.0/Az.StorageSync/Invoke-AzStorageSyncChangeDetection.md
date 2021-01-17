---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 9b7c539074f38b730a8ab5cd767a62fb44216ef6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427669"
---
# <span data-ttu-id="1b710-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="1b710-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="1b710-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b710-102">SYNOPSIS</span></span>
<span data-ttu-id="1b710-103">Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces.</span><span class="sxs-lookup"><span data-stu-id="1b710-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="1b710-104">Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1b710-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="1b710-105">No máximo 10.000 itens podem ser detectados.</span><span class="sxs-lookup"><span data-stu-id="1b710-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="1b710-106">Se o escopo das alterações for conhecido, limite a execução desse comando para partes do namespace, para que a detecção de alteração possa terminar rapidamente e dentro do limite de itens do 10.000.</span><span class="sxs-lookup"><span data-stu-id="1b710-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="1b710-107">O cmdlet Invoke-AzStorageSyncChangeDetection não irá detectar as seguintes alterações no compartilhamento de arquivos do Azure:</span><span class="sxs-lookup"><span data-stu-id="1b710-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="1b710-108">Arquivos que são excluídos.</span><span class="sxs-lookup"><span data-stu-id="1b710-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="1b710-109">Arquivos que são movidos do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1b710-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="1b710-110">Arquivos que são excluídos e criados com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="1b710-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="1b710-111">Essas alterações serão detectadas quando o [trabalho de detecção de alterações](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) for executado.</span><span class="sxs-lookup"><span data-stu-id="1b710-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="1b710-112">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b710-112">SYNTAX</span></span>

### <span data-ttu-id="1b710-113">StringAndDirectoryParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b710-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b710-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b710-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b710-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b710-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b710-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b710-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b710-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b710-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b710-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b710-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b710-119">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b710-119">DESCRIPTION</span></span>
<span data-ttu-id="1b710-120">Periodicamente, a sincronização de arquivos do Azure verifica o namespace dentro de um compartilhamento de arquivos do Azure de sincronização para as alterações que chegavam ao compartilhamento de arquivos por outros meios do que a sincronização. O objetivo é identificar essas alterações e, em última análise, sincronizá-las com os servidores conectados.</span><span class="sxs-lookup"><span data-stu-id="1b710-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="1b710-121">Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces.</span><span class="sxs-lookup"><span data-stu-id="1b710-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="1b710-122">Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1b710-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="1b710-123">Se o escopo das alterações for conhecido, limite a execução desse comando para partes do namespace, para que a detecção de alteração possa terminar rapidamente e dentro do limite de itens do 10.000.</span><span class="sxs-lookup"><span data-stu-id="1b710-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="1b710-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b710-124">EXAMPLES</span></span>

### <span data-ttu-id="1b710-125">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b710-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="1b710-126">Neste exemplo, a detecção de alterações é executada nos diretórios "dados" e "Reporting\Templates" de um compartilhamento de arquivos do Azure em sincronização.</span><span class="sxs-lookup"><span data-stu-id="1b710-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="1b710-127">Todos os caminhos são relativos à raiz do namespace do compartilhamento de arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b710-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="1b710-128">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1b710-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="1b710-129">Neste exemplo, a detecção de alterações é executada para um conjunto de arquivos conhecidos pelo chamador de comando que foram alterados.</span><span class="sxs-lookup"><span data-stu-id="1b710-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="1b710-130">O objetivo é fazer com que o Azure File Sync detecte e sincronize essas alterações também.</span><span class="sxs-lookup"><span data-stu-id="1b710-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="1b710-131">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1b710-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="1b710-132">Neste exemplo, a detecção de alterações é executada para o diretório "exemplos" e detecta recursivamente as alterações em subpastas.</span><span class="sxs-lookup"><span data-stu-id="1b710-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="1b710-133">Tenha em mente que o cmdlet falhará se o caminho contiver mais de 10.000 itens.</span><span class="sxs-lookup"><span data-stu-id="1b710-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="1b710-134">Se o caminho contiver mais de 10.000 itens, execute o comando em subpartes do namespace.</span><span class="sxs-lookup"><span data-stu-id="1b710-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="1b710-135">OS</span><span class="sxs-lookup"><span data-stu-id="1b710-135">PARAMETERS</span></span>

### <span data-ttu-id="1b710-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b710-136">-AsJob</span></span>
<span data-ttu-id="1b710-137">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1b710-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b710-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b710-138">-DefaultProfile</span></span>
<span data-ttu-id="1b710-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b710-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b710-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="1b710-140">-DirectoryPath</span></span>
<span data-ttu-id="1b710-141">Diretório em que a detecção de alterações será realizada.</span><span class="sxs-lookup"><span data-stu-id="1b710-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="1b710-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b710-142">-InputObject</span></span>
<span data-ttu-id="1b710-143">Objeto CloudEndpoint, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1b710-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1b710-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b710-144">-Name</span></span>
<span data-ttu-id="1b710-145">Nome do CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1b710-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="1b710-146">O nome é um GUID, não o nome amigável exibido no Portal.</span><span class="sxs-lookup"><span data-stu-id="1b710-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="1b710-147">Para obter o CloudEndpointName, use o cmdlet Get-AzStorageSyncCloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1b710-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="1b710-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b710-148">-PassThru</span></span>
<span data-ttu-id="1b710-149">Na execução normal, esse cmdlet retorna nenhum valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="1b710-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="1b710-150">Se você fornecer o parâmetro PassThru, o cmdlet irá escrever um valor para o pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1b710-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="1b710-151">-Caminho</span><span class="sxs-lookup"><span data-stu-id="1b710-151">-Path</span></span>
<span data-ttu-id="1b710-152">Caminho onde a detecção de alterações será realizada.</span><span class="sxs-lookup"><span data-stu-id="1b710-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="1b710-153">-Recursiva</span><span class="sxs-lookup"><span data-stu-id="1b710-153">-Recursive</span></span>
<span data-ttu-id="1b710-154">Indicação se a detecção de alterações de diretório é recursiva.</span><span class="sxs-lookup"><span data-stu-id="1b710-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="1b710-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b710-155">-ResourceGroupName</span></span>
<span data-ttu-id="1b710-156">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b710-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="1b710-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b710-157">-ResourceId</span></span>
<span data-ttu-id="1b710-158">ID do recurso CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="1b710-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="1b710-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="1b710-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="1b710-160">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="1b710-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="1b710-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1b710-161">-SyncGroupName</span></span>
<span data-ttu-id="1b710-162">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="1b710-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="1b710-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1b710-163">-Confirm</span></span>
<span data-ttu-id="1b710-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b710-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b710-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b710-165">-WhatIf</span></span>
<span data-ttu-id="1b710-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1b710-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b710-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b710-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b710-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b710-168">CommonParameters</span></span>
<span data-ttu-id="1b710-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b710-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b710-170">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b710-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b710-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b710-171">INPUTS</span></span>

### <span data-ttu-id="1b710-172">System. String</span><span class="sxs-lookup"><span data-stu-id="1b710-172">System.String</span></span>

### <span data-ttu-id="1b710-173">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1b710-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="1b710-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b710-174">OUTPUTS</span></span>

### <span data-ttu-id="1b710-175">System. void</span><span class="sxs-lookup"><span data-stu-id="1b710-175">System.Void</span></span>

## <span data-ttu-id="1b710-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b710-176">NOTES</span></span>

## <span data-ttu-id="1b710-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b710-177">RELATED LINKS</span></span>
