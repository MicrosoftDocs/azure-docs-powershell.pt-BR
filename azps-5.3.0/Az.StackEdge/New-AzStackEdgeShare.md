---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426724"
---
# <span data-ttu-id="d5fa1-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="d5fa1-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="d5fa1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fa1-103">Cria um novo compartilhamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5fa1-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="d5fa1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5fa1-104">SYNTAX</span></span>

### <span data-ttu-id="d5fa1-105">SmbParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5fa1-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5fa1-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5fa1-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5fa1-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5fa1-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5fa1-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5fa1-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5fa1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5fa1-109">DESCRIPTION</span></span>
<span data-ttu-id="d5fa1-110">O cmdlet **New-AzStackEdgeShare** cria um novo compartilhamento no dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="d5fa1-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="d5fa1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5fa1-111">EXAMPLES</span></span>

### <span data-ttu-id="d5fa1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5fa1-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="d5fa1-113">OS</span><span class="sxs-lookup"><span data-stu-id="d5fa1-113">PARAMETERS</span></span>

### <span data-ttu-id="d5fa1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5fa1-114">-AsJob</span></span>
<span data-ttu-id="d5fa1-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d5fa1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5fa1-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="d5fa1-116">-ClientAccessRight</span></span>
<span data-ttu-id="d5fa1-117">Acesso de leitura/gravação para clientIds, por exemplo: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="d5fa1-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="d5fa1-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="d5fa1-118">-CloudShare</span></span>
<span data-ttu-id="d5fa1-119">Fornecer o nome do recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="d5fa1-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="d5fa1-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d5fa1-120">-ContainerName</span></span>
<span data-ttu-id="d5fa1-121">Nome do contêiner (com base no formato de dados especificado, representa o nome do Azure files/Pageblob/Block BLOB)</span><span class="sxs-lookup"><span data-stu-id="d5fa1-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="d5fa1-122">-Formato DataFormat</span><span class="sxs-lookup"><span data-stu-id="d5fa1-122">-DataFormat</span></span>
<span data-ttu-id="d5fa1-123">Definir formato de dados por exemplo: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="d5fa1-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="d5fa1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fa1-124">-DefaultProfile</span></span>
<span data-ttu-id="d5fa1-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5fa1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5fa1-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d5fa1-126">-DeviceName</span></span>
<span data-ttu-id="d5fa1-127">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="d5fa1-127">Device Name</span></span>

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

### <span data-ttu-id="d5fa1-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5fa1-128">-Name</span></span>
<span data-ttu-id="d5fa1-129">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="d5fa1-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fa1-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="d5fa1-130">-NFS</span></span>
<span data-ttu-id="d5fa1-131">AccessProtocol no caso da criação de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="d5fa1-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="d5fa1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5fa1-132">-ResourceGroupName</span></span>
<span data-ttu-id="d5fa1-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d5fa1-133">Resource Group Name</span></span>

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

### <span data-ttu-id="d5fa1-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="d5fa1-134">-SMB</span></span>
<span data-ttu-id="d5fa1-135">AccessProtocol no caso da criação de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="d5fa1-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="d5fa1-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="d5fa1-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="d5fa1-137">Fornecer o nome do recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="d5fa1-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fa1-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="d5fa1-138">-UserAccessRight</span></span>
<span data-ttu-id="d5fa1-139">forneça acesso à direita juntamente com nomes de usuário existentes para acessar tipos de compartilhamento SMB, por exemplo: @ (@ {"nome_do_usuário" = "User-Name-1"; " AccessRight "=" ler "}, @ {" username "=" User-Name-2 ";" AccessRight "=" ler "}, @ {" username "=" User-Name-3 ";" AccessRight "=" personalizado "})</span><span class="sxs-lookup"><span data-stu-id="d5fa1-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="d5fa1-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d5fa1-140">-Confirm</span></span>
<span data-ttu-id="d5fa1-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5fa1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5fa1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5fa1-142">-WhatIf</span></span>
<span data-ttu-id="d5fa1-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d5fa1-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5fa1-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5fa1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5fa1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fa1-145">CommonParameters</span></span>
<span data-ttu-id="d5fa1-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5fa1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fa1-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5fa1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fa1-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5fa1-148">INPUTS</span></span>

### <span data-ttu-id="d5fa1-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d5fa1-149">System.String</span></span>

## <span data-ttu-id="d5fa1-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5fa1-150">OUTPUTS</span></span>

### <span data-ttu-id="d5fa1-151">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="d5fa1-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="d5fa1-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5fa1-152">NOTES</span></span>

## <span data-ttu-id="d5fa1-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5fa1-153">RELATED LINKS</span></span>
