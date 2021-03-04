---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
ms.openlocfilehash: bfccf106d2dbc541f9887fddff12bd512640f55c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888712"
---
# <span data-ttu-id="38abd-101">New-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="38abd-101">New-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="38abd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38abd-102">SYNOPSIS</span></span>
<span data-ttu-id="38abd-103">Cria um novo compartilhamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38abd-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="38abd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38abd-104">SYNTAX</span></span>

### <span data-ttu-id="38abd-105">SmbParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="38abd-105">SmbParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38abd-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="38abd-106">CloudShareNfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38abd-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="38abd-107">CloudShareSmbParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38abd-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="38abd-108">NfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38abd-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38abd-109">DESCRIPTION</span></span>
<span data-ttu-id="38abd-110">O cmdlet **New-AzDataBoxEdgeShare** cria um novo compartilhamento no dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="38abd-110">The **New-AzDataBoxEdgeShare** cmdlet creates a new share on the Data Box Edge device.</span></span>

## <span data-ttu-id="38abd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38abd-111">EXAMPLES</span></span>

### <span data-ttu-id="38abd-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38abd-112">Example 1</span></span>
```
PS C:\> New-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="38abd-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38abd-113">PARAMETERS</span></span>

### <span data-ttu-id="38abd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38abd-114">-AsJob</span></span>
<span data-ttu-id="38abd-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="38abd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38abd-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="38abd-116">-ClientAccessRight</span></span>
<span data-ttu-id="38abd-117">Acesso de leitura/gravação para clientIds, para ex:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="38abd-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="38abd-118">-CloudShare</span></span>
<span data-ttu-id="38abd-119">Fornecer o Nome de Recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="38abd-119">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="38abd-120">-ContainerName</span></span>
<span data-ttu-id="38abd-121">Nome do contêiner (Com base no formato de dados especificado, isso representa o nome dos arquivos do Azure/pageblob/blob de bloqueio)</span><span class="sxs-lookup"><span data-stu-id="38abd-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="38abd-122">-DataFormat</span></span>
<span data-ttu-id="38abd-123">Definir Formato de Dados ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="38abd-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38abd-124">-DefaultProfile</span></span>
<span data-ttu-id="38abd-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38abd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38abd-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="38abd-126">-DeviceName</span></span>
<span data-ttu-id="38abd-127">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="38abd-127">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-128">-Name</span><span class="sxs-lookup"><span data-stu-id="38abd-128">-Name</span></span>
<span data-ttu-id="38abd-129">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="38abd-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="38abd-130">-NFS</span></span>
<span data-ttu-id="38abd-131">AccessProtocol no caso de criar o Share</span><span class="sxs-lookup"><span data-stu-id="38abd-131">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38abd-132">-ResourceGroupName</span></span>
<span data-ttu-id="38abd-133">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="38abd-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="38abd-134">-SMB</span></span>
<span data-ttu-id="38abd-135">AccessProtocol no caso de criar o Share</span><span class="sxs-lookup"><span data-stu-id="38abd-135">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="38abd-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="38abd-137">Fornecer o Nome de Recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="38abd-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="38abd-138">-UserAccessRight</span></span>
<span data-ttu-id="38abd-139">forneça acesso à direita juntamente com os nomes de usuário existentes para acessar tipos de Compartilhamento SMB, para ex: @(@{"Username"="user-name-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="38abd-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38abd-140">-Confirm</span></span>
<span data-ttu-id="38abd-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38abd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38abd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38abd-142">-WhatIf</span></span>
<span data-ttu-id="38abd-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38abd-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38abd-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38abd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38abd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38abd-145">CommonParameters</span></span>
<span data-ttu-id="38abd-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38abd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38abd-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38abd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38abd-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38abd-148">INPUTS</span></span>

### <span data-ttu-id="38abd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="38abd-149">System.String</span></span>

## <span data-ttu-id="38abd-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38abd-150">OUTPUTS</span></span>

### <span data-ttu-id="38abd-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="38abd-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="38abd-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="38abd-152">NOTES</span></span>

## <span data-ttu-id="38abd-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38abd-153">RELATED LINKS</span></span>
