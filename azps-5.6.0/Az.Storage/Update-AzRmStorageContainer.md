---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 696070e19f1810ab352abde4ad6248f4bf42b180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888051"
---
# <span data-ttu-id="3a2e1-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a2e1-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="3a2e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a2e1-102">SYNOPSIS</span></span>
<span data-ttu-id="3a2e1-103">Modifica um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a2e1-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="3a2e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3a2e1-104">SYNTAX</span></span>

### <span data-ttu-id="3a2e1-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3a2e1-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a2e1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3a2e1-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a2e1-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="3a2e1-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a2e1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3a2e1-108">DESCRIPTION</span></span>
<span data-ttu-id="3a2e1-109">O cmdlet **Update-AzRmStorageContainer** modifica um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a2e1-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="3a2e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a2e1-110">EXAMPLES</span></span>

### <span data-ttu-id="3a2e1-111">Exemplo 1: modifica os metadados de um contêiner de blob de armazenamento e o acesso público com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="3a2e1-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="3a2e1-112">Este comando modifica os metadados de um contêiner de blob de armazenamento e o acesso público com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="3a2e1-113">Exemplo 2: Desabilitar o acesso público em um contêiner de blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="3a2e1-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="3a2e1-114">Este comando desabilita o acesso público em um contêiner de blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="3a2e1-115">Exemplo 3: definir o acesso público como Blob para todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="3a2e1-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="3a2e1-116">Este comando definiu o acesso público como Blob para todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="3a2e1-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3a2e1-117">PARAMETERS</span></span>

### <span data-ttu-id="3a2e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a2e1-118">-DefaultProfile</span></span>
<span data-ttu-id="3a2e1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a2e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a2e1-120">-InputObject</span></span>
<span data-ttu-id="3a2e1-121">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a2e1-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a2e1-122">-Metadados</span><span class="sxs-lookup"><span data-stu-id="3a2e1-122">-Metadata</span></span>
<span data-ttu-id="3a2e1-123">Metadados de Contêiner</span><span class="sxs-lookup"><span data-stu-id="3a2e1-123">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a2e1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3a2e1-124">-Name</span></span>
<span data-ttu-id="3a2e1-125">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="3a2e1-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a2e1-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="3a2e1-126">-PublicAccess</span></span>
<span data-ttu-id="3a2e1-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="3a2e1-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a2e1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a2e1-128">-ResourceGroupName</span></span>
<span data-ttu-id="3a2e1-129">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a2e1-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e1-130">-StorageAccount</span></span>
<span data-ttu-id="3a2e1-131">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a2e1-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a2e1-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3a2e1-132">-StorageAccountName</span></span>
<span data-ttu-id="3a2e1-133">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a2e1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a2e1-134">-Confirm</span></span>
<span data-ttu-id="3a2e1-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a2e1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a2e1-136">-WhatIf</span></span>
<span data-ttu-id="3a2e1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a2e1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a2e1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a2e1-139">CommonParameters</span></span>
<span data-ttu-id="3a2e1-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a2e1-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a2e1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a2e1-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a2e1-142">INPUTS</span></span>

### <span data-ttu-id="3a2e1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3a2e1-143">System.String</span></span>

### <span data-ttu-id="3a2e1-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e1-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3a2e1-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="3a2e1-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="3a2e1-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3a2e1-146">OUTPUTS</span></span>

### <span data-ttu-id="3a2e1-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="3a2e1-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="3a2e1-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="3a2e1-148">NOTES</span></span>

## <span data-ttu-id="3a2e1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a2e1-149">RELATED LINKS</span></span>
