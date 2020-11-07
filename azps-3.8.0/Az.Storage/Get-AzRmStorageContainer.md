---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: da0ccdc791318f0a315bea8d2464d8d0852aec8b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942304"
---
# <span data-ttu-id="20bbf-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="20bbf-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="20bbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="20bbf-103">Obtém ou lista contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="20bbf-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="20bbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20bbf-104">SYNTAX</span></span>

### <span data-ttu-id="20bbf-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="20bbf-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20bbf-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="20bbf-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20bbf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20bbf-107">DESCRIPTION</span></span>
<span data-ttu-id="20bbf-108">O cmdlet **Get-AzRmStorageContainer** Obtém ou lista os contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="20bbf-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="20bbf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20bbf-109">EXAMPLES</span></span>

### <span data-ttu-id="20bbf-110">Exemplo 1: obter um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="20bbf-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="20bbf-111">Esse comando obtém um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="20bbf-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="20bbf-112">Exemplo 2: listar todos os contêineres de blob de armazenamento de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="20bbf-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="20bbf-113">Esse comando lista todos os contêineres de armazenamento de blob de uma conta de armazenamento com o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20bbf-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="20bbf-114">Exemplo 3: obter um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="20bbf-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="20bbf-115">Esse comando obtém um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="20bbf-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="20bbf-116">OS</span><span class="sxs-lookup"><span data-stu-id="20bbf-116">PARAMETERS</span></span>

### <span data-ttu-id="20bbf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20bbf-117">-AsJob</span></span>
<span data-ttu-id="20bbf-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="20bbf-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20bbf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20bbf-119">-DefaultProfile</span></span>
<span data-ttu-id="20bbf-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20bbf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20bbf-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="20bbf-121">-Name</span></span>
<span data-ttu-id="20bbf-122">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="20bbf-122">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20bbf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20bbf-123">-ResourceGroupName</span></span>
<span data-ttu-id="20bbf-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="20bbf-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="20bbf-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="20bbf-125">-StorageAccount</span></span>
<span data-ttu-id="20bbf-126">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="20bbf-126">Storage account object</span></span>

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

### <span data-ttu-id="20bbf-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="20bbf-127">-StorageAccountName</span></span>
<span data-ttu-id="20bbf-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20bbf-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="20bbf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20bbf-129">CommonParameters</span></span>
<span data-ttu-id="20bbf-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20bbf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20bbf-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20bbf-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20bbf-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20bbf-132">INPUTS</span></span>

### <span data-ttu-id="20bbf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="20bbf-133">System.String</span></span>

### <span data-ttu-id="20bbf-134">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20bbf-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="20bbf-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20bbf-135">OUTPUTS</span></span>

### <span data-ttu-id="20bbf-136">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="20bbf-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="20bbf-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20bbf-137">NOTES</span></span>

## <span data-ttu-id="20bbf-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20bbf-138">RELATED LINKS</span></span>
