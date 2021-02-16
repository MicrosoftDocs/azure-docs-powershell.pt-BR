---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113687"
---
# <span data-ttu-id="43fa4-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="43fa4-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="43fa4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="43fa4-103">Cria um novo compartilhamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43fa4-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="43fa4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43fa4-104">SYNTAX</span></span>

### <span data-ttu-id="43fa4-105">SmbParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="43fa4-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43fa4-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="43fa4-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43fa4-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="43fa4-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43fa4-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="43fa4-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43fa4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="43fa4-109">DESCRIPTION</span></span>
<span data-ttu-id="43fa4-110">O cmdlet **New-AzSt stackEdgeShare** cria um novo compartilhamento no dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="43fa4-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="43fa4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43fa4-111">EXAMPLES</span></span>

### <span data-ttu-id="43fa4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43fa4-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="43fa4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43fa4-113">PARAMETERS</span></span>

### <span data-ttu-id="43fa4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43fa4-114">-AsJob</span></span>
<span data-ttu-id="43fa4-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="43fa4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43fa4-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="43fa4-116">-ClientAccessRight</span></span>
<span data-ttu-id="43fa4-117">Acesso de leitura/gravação para clientIds, Para ex:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="43fa4-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="43fa4-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="43fa4-118">-CloudShare</span></span>
<span data-ttu-id="43fa4-119">Fornecer o Nome de Recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="43fa4-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="43fa4-120">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="43fa4-120">-ContainerName</span></span>
<span data-ttu-id="43fa4-121">Nome do contêiner (com base no formato de dados especificado, isso representa o nome dos Arquivos do Azure/Pageb ltd/Blob)</span><span class="sxs-lookup"><span data-stu-id="43fa4-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="43fa4-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="43fa4-122">-DataFormat</span></span>
<span data-ttu-id="43fa4-123">Definir Formato de Dados, por ex: PageB ltd, BlobBlab</span><span class="sxs-lookup"><span data-stu-id="43fa4-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="43fa4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43fa4-124">-DefaultProfile</span></span>
<span data-ttu-id="43fa4-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43fa4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43fa4-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="43fa4-126">-DeviceName</span></span>
<span data-ttu-id="43fa4-127">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="43fa4-127">Device Name</span></span>

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

### <span data-ttu-id="43fa4-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="43fa4-128">-Name</span></span>
<span data-ttu-id="43fa4-129">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="43fa4-129">Resource Name</span></span>

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

### <span data-ttu-id="43fa4-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="43fa4-130">-NFS</span></span>
<span data-ttu-id="43fa4-131">AccessProtocol no caso de criar o Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="43fa4-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="43fa4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43fa4-132">-ResourceGroupName</span></span>
<span data-ttu-id="43fa4-133">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="43fa4-133">Resource Group Name</span></span>

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

### <span data-ttu-id="43fa4-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="43fa4-134">-SMB</span></span>
<span data-ttu-id="43fa4-135">AccessProtocol no caso de criar o Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="43fa4-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="43fa4-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="43fa4-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="43fa4-137">Fornecer o Nome de Recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="43fa4-137">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="43fa4-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="43fa4-138">-UserAccessRight</span></span>
<span data-ttu-id="43fa4-139">fornecer acesso à direita juntamente com os nomes de usuário existentes para acessar os tipos de Compartilhamento SMB, por exemplo: @(@{"Nome de usuário"="nome de usuário-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="43fa4-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="43fa4-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="43fa4-140">-Confirm</span></span>
<span data-ttu-id="43fa4-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43fa4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43fa4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43fa4-142">-WhatIf</span></span>
<span data-ttu-id="43fa4-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="43fa4-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43fa4-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43fa4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43fa4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fa4-145">CommonParameters</span></span>
<span data-ttu-id="43fa4-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43fa4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fa4-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43fa4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fa4-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="43fa4-148">INPUTS</span></span>

### <span data-ttu-id="43fa4-149">System.String</span><span class="sxs-lookup"><span data-stu-id="43fa4-149">System.String</span></span>

## <span data-ttu-id="43fa4-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="43fa4-150">OUTPUTS</span></span>

### <span data-ttu-id="43fa4-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="43fa4-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="43fa4-152">Notas</span><span class="sxs-lookup"><span data-stu-id="43fa4-152">NOTES</span></span>

## <span data-ttu-id="43fa4-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43fa4-153">RELATED LINKS</span></span>
