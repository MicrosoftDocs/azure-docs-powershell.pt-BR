---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427121"
---
# <span data-ttu-id="b9ce1-101">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b9ce1-101">Get-AzureRmStorageContainer</span></span>

## <span data-ttu-id="b9ce1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ce1-103">Obtém ou lista contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b9ce1-103">Gets or lists Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9ce1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9ce1-104">SYNTAX</span></span>

### <span data-ttu-id="b9ce1-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9ce1-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9ce1-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="b9ce1-106">AccountObject</span></span>
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9ce1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9ce1-107">DESCRIPTION</span></span>
<span data-ttu-id="b9ce1-108">O cmdlet **Get-AzureRmStorageContainer** Obtém ou lista os contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b9ce1-108">The **Get-AzureRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="b9ce1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9ce1-109">EXAMPLES</span></span>

### <span data-ttu-id="b9ce1-110">Exemplo 1: obter um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="b9ce1-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

<span data-ttu-id="b9ce1-111">Esse comando obtém um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="b9ce1-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b9ce1-112">Exemplo 2: listar todos os contêineres de blob de armazenamento de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b9ce1-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

<span data-ttu-id="b9ce1-113">Esse comando lista todos os contêineres de armazenamento de blob de uma conta de armazenamento com o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b9ce1-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="b9ce1-114">Exemplo 3: obter um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="b9ce1-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

<span data-ttu-id="b9ce1-115">Esse comando obtém um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="b9ce1-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="b9ce1-116">OS</span><span class="sxs-lookup"><span data-stu-id="b9ce1-116">PARAMETERS</span></span>

### <span data-ttu-id="b9ce1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ce1-117">-DefaultProfile</span></span>
<span data-ttu-id="b9ce1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ce1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9ce1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9ce1-119">-Name</span></span>
<span data-ttu-id="b9ce1-120">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="b9ce1-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9ce1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ce1-121">-ResourceGroupName</span></span>
<span data-ttu-id="b9ce1-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9ce1-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="b9ce1-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9ce1-123">-StorageAccount</span></span>
<span data-ttu-id="b9ce1-124">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b9ce1-124">Storage account object</span></span>

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

### <span data-ttu-id="b9ce1-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b9ce1-125">-StorageAccountName</span></span>
<span data-ttu-id="b9ce1-126">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b9ce1-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="b9ce1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ce1-127">CommonParameters</span></span>
<span data-ttu-id="b9ce1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ce1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ce1-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9ce1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ce1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9ce1-130">INPUTS</span></span>

### <span data-ttu-id="b9ce1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b9ce1-131">System.String</span></span>

## <span data-ttu-id="b9ce1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9ce1-132">OUTPUTS</span></span>

### <span data-ttu-id="b9ce1-133">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="b9ce1-133">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="b9ce1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9ce1-134">NOTES</span></span>

## <span data-ttu-id="b9ce1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9ce1-135">RELATED LINKS</span></span>

