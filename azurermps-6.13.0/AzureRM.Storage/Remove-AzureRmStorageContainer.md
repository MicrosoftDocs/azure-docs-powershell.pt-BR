---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
ms.openlocfilehash: 089451a0a0aae399a18296fbf4982724b35d432e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610529"
---
# <span data-ttu-id="74b90-101">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="74b90-101">Remove-AzureRmStorageContainer</span></span>

## <span data-ttu-id="74b90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74b90-102">SYNOPSIS</span></span>
<span data-ttu-id="74b90-103">Remove um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="74b90-103">Removes a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74b90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74b90-104">SYNTAX</span></span>

### <span data-ttu-id="74b90-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="74b90-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74b90-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="74b90-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74b90-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="74b90-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74b90-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74b90-108">DESCRIPTION</span></span>
<span data-ttu-id="74b90-109">O cmdlet **Remove-AzureRmStorageContainer** remove um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="74b90-109">The **Remove-AzureRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="74b90-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74b90-110">EXAMPLES</span></span>

### <span data-ttu-id="74b90-111">Exemplo 1: remover um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="74b90-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="74b90-112">Esse comando Remove um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="74b90-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="74b90-113">Exemplo 2: remover um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="74b90-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="74b90-114">Esse comando Remove um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="74b90-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="74b90-115">Exemplo 3: remover todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="74b90-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainer -Force
```

<span data-ttu-id="74b90-116">Esse comando Remove todos os contêineres de armazenamento de BLOB em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="74b90-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="74b90-117">OS</span><span class="sxs-lookup"><span data-stu-id="74b90-117">PARAMETERS</span></span>

### <span data-ttu-id="74b90-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b90-118">-DefaultProfile</span></span>
<span data-ttu-id="74b90-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74b90-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74b90-120">-Force</span><span class="sxs-lookup"><span data-stu-id="74b90-120">-Force</span></span>
<span data-ttu-id="74b90-121">Forçar a remoção do contêiner e todo o conteúdo dele</span><span class="sxs-lookup"><span data-stu-id="74b90-121">Force to remove the container and all content in it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b90-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74b90-122">-InputObject</span></span>
<span data-ttu-id="74b90-123">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="74b90-123">Storage container object</span></span>

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

### <span data-ttu-id="74b90-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="74b90-124">-Name</span></span>
<span data-ttu-id="74b90-125">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="74b90-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74b90-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74b90-126">-PassThru</span></span>
<span data-ttu-id="74b90-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="74b90-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b90-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b90-128">-ResourceGroupName</span></span>
<span data-ttu-id="74b90-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74b90-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="74b90-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="74b90-130">-StorageAccount</span></span>
<span data-ttu-id="74b90-131">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="74b90-131">Storage account object</span></span>

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

### <span data-ttu-id="74b90-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="74b90-132">-StorageAccountName</span></span>
<span data-ttu-id="74b90-133">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="74b90-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="74b90-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="74b90-134">-Confirm</span></span>
<span data-ttu-id="74b90-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74b90-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b90-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b90-136">-WhatIf</span></span>
<span data-ttu-id="74b90-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74b90-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74b90-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74b90-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b90-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b90-139">CommonParameters</span></span>
<span data-ttu-id="74b90-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b90-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b90-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74b90-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b90-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74b90-142">INPUTS</span></span>

### <span data-ttu-id="74b90-143">System. String</span><span class="sxs-lookup"><span data-stu-id="74b90-143">System.String</span></span>

## <span data-ttu-id="74b90-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74b90-144">OUTPUTS</span></span>

### <span data-ttu-id="74b90-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="74b90-145">System.Object</span></span>

## <span data-ttu-id="74b90-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74b90-146">NOTES</span></span>

## <span data-ttu-id="74b90-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74b90-147">RELATED LINKS</span></span>
