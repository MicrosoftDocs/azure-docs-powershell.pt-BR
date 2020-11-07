---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: f54196ef5b055a5e1968c682d21f861ee41c77ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774071"
---
# <span data-ttu-id="60d49-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="60d49-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="60d49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60d49-102">SYNOPSIS</span></span>
<span data-ttu-id="60d49-103">Obtém ou lista compartilhamentos de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60d49-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="60d49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60d49-104">SYNTAX</span></span>

### <span data-ttu-id="60d49-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="60d49-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60d49-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="60d49-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60d49-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="60d49-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60d49-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60d49-108">DESCRIPTION</span></span>
<span data-ttu-id="60d49-109">O cmdlet **Get-AzRmStorageShare** Obtém ou lista os compartilhamentos de arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60d49-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="60d49-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60d49-110">EXAMPLES</span></span>

### <span data-ttu-id="60d49-111">Exemplo 1: obter um compartilhamento de arquivos de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="60d49-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="60d49-112">Este comando obtém um compartilhamento de arquivo de armazenamento com o nome da conta de armazenamento e o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="60d49-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="60d49-113">Exemplo 2: listar todos os compartilhamentos de arquivos de armazenamento de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60d49-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="60d49-114">Esse comando lista todos os compartilhamentos de arquivos de armazenamento de uma conta de armazenamento com o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60d49-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="60d49-115">Exemplo 3: obter um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="60d49-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="60d49-116">Esse comando obtém um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="60d49-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="60d49-117">OS</span><span class="sxs-lookup"><span data-stu-id="60d49-117">PARAMETERS</span></span>

### <span data-ttu-id="60d49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d49-118">-DefaultProfile</span></span>
<span data-ttu-id="60d49-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60d49-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60d49-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="60d49-120">-Name</span></span>
<span data-ttu-id="60d49-121">Nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="60d49-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60d49-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60d49-122">-ResourceGroupName</span></span>
<span data-ttu-id="60d49-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60d49-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="60d49-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60d49-124">-ResourceId</span></span>
<span data-ttu-id="60d49-125">Insira uma ID de recurso de compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="60d49-125">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d49-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="60d49-126">-StorageAccount</span></span>
<span data-ttu-id="60d49-127">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60d49-127">Storage account object</span></span>

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

### <span data-ttu-id="60d49-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="60d49-128">-StorageAccountName</span></span>
<span data-ttu-id="60d49-129">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60d49-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="60d49-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d49-130">CommonParameters</span></span>
<span data-ttu-id="60d49-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d49-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d49-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60d49-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d49-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60d49-133">INPUTS</span></span>

### <span data-ttu-id="60d49-134">System. String</span><span class="sxs-lookup"><span data-stu-id="60d49-134">System.String</span></span>

### <span data-ttu-id="60d49-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60d49-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="60d49-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60d49-136">OUTPUTS</span></span>

### <span data-ttu-id="60d49-137">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="60d49-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="60d49-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60d49-138">NOTES</span></span>

## <span data-ttu-id="60d49-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60d49-139">RELATED LINKS</span></span>
