---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: aa2a03355431f027a9efd374f5af45199cc77452
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774058"
---
# <span data-ttu-id="9c248-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9c248-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="9c248-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c248-102">SYNOPSIS</span></span>
<span data-ttu-id="9c248-103">Obtém ou lista contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9c248-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="9c248-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c248-104">SYNTAX</span></span>

### <span data-ttu-id="9c248-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c248-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c248-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="9c248-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c248-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c248-107">DESCRIPTION</span></span>
<span data-ttu-id="9c248-108">O cmdlet **Get-AzRmStorageContainer** Obtém ou lista os contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9c248-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="9c248-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c248-109">EXAMPLES</span></span>

### <span data-ttu-id="9c248-110">Exemplo 1: obter um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="9c248-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="9c248-111">Esse comando obtém um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9c248-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="9c248-112">Exemplo 2: listar todos os contêineres de blob de armazenamento de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9c248-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="9c248-113">Esse comando lista todos os contêineres de armazenamento de blob de uma conta de armazenamento com o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c248-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="9c248-114">Exemplo 3: obter um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9c248-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="9c248-115">Esse comando obtém um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9c248-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="9c248-116">OS</span><span class="sxs-lookup"><span data-stu-id="9c248-116">PARAMETERS</span></span>

### <span data-ttu-id="9c248-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c248-117">-AsJob</span></span>
<span data-ttu-id="9c248-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9c248-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c248-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c248-119">-DefaultProfile</span></span>
<span data-ttu-id="9c248-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c248-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c248-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c248-121">-Name</span></span>
<span data-ttu-id="9c248-122">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="9c248-122">Container Name</span></span>

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

### <span data-ttu-id="9c248-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c248-123">-ResourceGroupName</span></span>
<span data-ttu-id="9c248-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c248-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="9c248-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9c248-125">-StorageAccount</span></span>
<span data-ttu-id="9c248-126">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9c248-126">Storage account object</span></span>

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

### <span data-ttu-id="9c248-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9c248-127">-StorageAccountName</span></span>
<span data-ttu-id="9c248-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c248-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="9c248-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c248-129">CommonParameters</span></span>
<span data-ttu-id="9c248-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c248-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c248-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c248-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c248-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c248-132">INPUTS</span></span>

### <span data-ttu-id="9c248-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9c248-133">System.String</span></span>

### <span data-ttu-id="9c248-134">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9c248-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9c248-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c248-135">OUTPUTS</span></span>

### <span data-ttu-id="9c248-136">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="9c248-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="9c248-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c248-137">NOTES</span></span>

## <span data-ttu-id="9c248-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c248-138">RELATED LINKS</span></span>
