---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
ms.openlocfilehash: 9e4f62ef28d4cbcb22ddb563e558ad5d48733360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431266"
---
# <span data-ttu-id="8b690-101">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8b690-101">Update-AzureRmStorageContainer</span></span>

## <span data-ttu-id="8b690-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b690-102">SYNOPSIS</span></span>
<span data-ttu-id="8b690-103">Modifica um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8b690-103">Modifies a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b690-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b690-104">SYNTAX</span></span>

### <span data-ttu-id="8b690-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b690-105">AccountName (Default)</span></span>
```
Update-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b690-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="8b690-106">AccountObject</span></span>
```
Update-AzureRmStorageContainer [-Name] <String> -StorageAccount <PSStorageAccount>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b690-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="8b690-107">ContainerObject</span></span>
```
Update-AzureRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b690-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b690-108">DESCRIPTION</span></span>
<span data-ttu-id="8b690-109">O cmdlet **Update-AzureRmStorageContainer** modifica um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8b690-109">The **Update-AzureRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="8b690-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b690-110">EXAMPLES</span></span>

### <span data-ttu-id="8b690-111">Exemplo 1: modifica os metadados e o acesso público de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="8b690-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"} 
```

<span data-ttu-id="8b690-112">Esse comando modifica os metadados e o acesso público do contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8b690-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="8b690-113">Exemplo 2: desabilitar o acesso público em um contêiner de blob de armazenamento com objeto da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="8b690-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="8b690-114">Esse comando desabilita o acesso público em um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8b690-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="8b690-115">Exemplo 3: definir o acesso público como blob para todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="8b690-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzureRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="8b690-116">Esse comando define o acesso público como blob para todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="8b690-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="8b690-117">OS</span><span class="sxs-lookup"><span data-stu-id="8b690-117">PARAMETERS</span></span>

### <span data-ttu-id="8b690-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b690-118">-DefaultProfile</span></span>
<span data-ttu-id="8b690-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b690-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b690-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b690-120">-InputObject</span></span>
<span data-ttu-id="8b690-121">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8b690-121">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b690-122">-Metadados</span><span class="sxs-lookup"><span data-stu-id="8b690-122">-Metadata</span></span>
<span data-ttu-id="8b690-123">Metadados do contêiner</span><span class="sxs-lookup"><span data-stu-id="8b690-123">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b690-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b690-124">-Name</span></span>
<span data-ttu-id="8b690-125">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="8b690-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b690-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="8b690-126">-PublicAccess</span></span>
<span data-ttu-id="8b690-127">PublicAccess de contêiner</span><span class="sxs-lookup"><span data-stu-id="8b690-127">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b690-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b690-128">-ResourceGroupName</span></span>
<span data-ttu-id="8b690-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b690-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b690-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b690-130">-StorageAccount</span></span>
<span data-ttu-id="8b690-131">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8b690-131">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b690-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b690-132">-StorageAccountName</span></span>
<span data-ttu-id="8b690-133">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8b690-133">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b690-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b690-134">-Confirm</span></span>
<span data-ttu-id="8b690-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b690-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b690-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b690-136">-WhatIf</span></span>
<span data-ttu-id="8b690-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b690-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b690-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b690-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b690-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b690-139">CommonParameters</span></span>
<span data-ttu-id="8b690-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b690-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b690-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b690-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b690-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b690-142">INPUTS</span></span>

### <span data-ttu-id="8b690-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8b690-143">System.String</span></span>

## <span data-ttu-id="8b690-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b690-144">OUTPUTS</span></span>

### <span data-ttu-id="8b690-145">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="8b690-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="8b690-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b690-146">NOTES</span></span>

## <span data-ttu-id="8b690-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b690-147">RELATED LINKS</span></span>

