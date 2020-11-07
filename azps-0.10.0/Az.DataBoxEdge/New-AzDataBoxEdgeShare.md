---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
ms.openlocfilehash: 19dd22f15400e99f95947d97fe8c46077911de61
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776765"
---
# <span data-ttu-id="dd253-101">New-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="dd253-101">New-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="dd253-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd253-102">SYNOPSIS</span></span>
<span data-ttu-id="dd253-103">Cria um novo compartilhamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd253-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="dd253-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd253-104">SYNTAX</span></span>

### <span data-ttu-id="dd253-105">SmbParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd253-105">SmbParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd253-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd253-106">CloudShareNfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd253-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd253-107">CloudShareSmbParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd253-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd253-108">NfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd253-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd253-109">DESCRIPTION</span></span>
<span data-ttu-id="dd253-110">O cmdlet **New-AzDataBoxEdgeShare** cria um novo compartilhamento no dispositivo de borda da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="dd253-110">The **New-AzDataBoxEdgeShare** cmdlet creates a new share on the Data Box Edge device.</span></span>

## <span data-ttu-id="dd253-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd253-111">EXAMPLES</span></span>

### <span data-ttu-id="dd253-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd253-112">Example 1</span></span>
```
PS C:\> New-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="dd253-113">OS</span><span class="sxs-lookup"><span data-stu-id="dd253-113">PARAMETERS</span></span>

### <span data-ttu-id="dd253-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd253-114">-AsJob</span></span>
<span data-ttu-id="dd253-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dd253-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd253-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="dd253-116">-ClientAccessRight</span></span>
<span data-ttu-id="dd253-117">Acesso de leitura/gravação para clientIds, por exemplo: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="dd253-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="dd253-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="dd253-118">-CloudShare</span></span>
<span data-ttu-id="dd253-119">Fornecer o nome do recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="dd253-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="dd253-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dd253-120">-ContainerName</span></span>
<span data-ttu-id="dd253-121">Nome do contêiner (com base no formato de dados especificado, representa o nome do Azure files/Pageblob/Block BLOB)</span><span class="sxs-lookup"><span data-stu-id="dd253-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="dd253-122">-Formato DataFormat</span><span class="sxs-lookup"><span data-stu-id="dd253-122">-DataFormat</span></span>
<span data-ttu-id="dd253-123">Definir formato de dados por exemplo: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="dd253-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="dd253-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd253-124">-DefaultProfile</span></span>
<span data-ttu-id="dd253-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd253-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd253-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dd253-126">-DeviceName</span></span>
<span data-ttu-id="dd253-127">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="dd253-127">Device Name</span></span>

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

### <span data-ttu-id="dd253-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd253-128">-Name</span></span>
<span data-ttu-id="dd253-129">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="dd253-129">Resource Name</span></span>

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

### <span data-ttu-id="dd253-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="dd253-130">-NFS</span></span>
<span data-ttu-id="dd253-131">AccessProtocol no caso da criação de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="dd253-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="dd253-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd253-132">-ResourceGroupName</span></span>
<span data-ttu-id="dd253-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dd253-133">Resource Group Name</span></span>

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

### <span data-ttu-id="dd253-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="dd253-134">-SMB</span></span>
<span data-ttu-id="dd253-135">AccessProtocol no caso da criação de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="dd253-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="dd253-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="dd253-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="dd253-137">Fornecer o nome do recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="dd253-137">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="dd253-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="dd253-138">-UserAccessRight</span></span>
<span data-ttu-id="dd253-139">forneça acesso à direita juntamente com nomes de usuário existentes para acessar tipos de compartilhamento SMB, por exemplo: @ (@ {"nome_do_usuário" = "User-Name-1"; " AccessRight "=" ler "}, @ {" username "=" User-Name-2 ";" AccessRight "=" ler "}, @ {" username "=" User-Name-3 ";" AccessRight "=" personalizado "})</span><span class="sxs-lookup"><span data-stu-id="dd253-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="dd253-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd253-140">-Confirm</span></span>
<span data-ttu-id="dd253-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd253-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd253-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd253-142">-WhatIf</span></span>
<span data-ttu-id="dd253-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd253-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd253-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd253-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd253-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd253-145">CommonParameters</span></span>
<span data-ttu-id="dd253-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd253-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd253-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd253-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd253-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd253-148">INPUTS</span></span>

### <span data-ttu-id="dd253-149">System. String</span><span class="sxs-lookup"><span data-stu-id="dd253-149">System.String</span></span>

## <span data-ttu-id="dd253-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd253-150">OUTPUTS</span></span>

### <span data-ttu-id="dd253-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="dd253-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="dd253-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd253-152">NOTES</span></span>

## <span data-ttu-id="dd253-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd253-153">RELATED LINKS</span></span>