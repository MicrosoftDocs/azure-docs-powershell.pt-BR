---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: c4f5fe5fa703d2706d37cd0bebf9df79fd272f5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892015"
---
# <span data-ttu-id="dcb56-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dcb56-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="dcb56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcb56-102">SYNOPSIS</span></span>
<span data-ttu-id="dcb56-103">Obtém ou lista Contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcb56-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="dcb56-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dcb56-104">SYNTAX</span></span>

### <span data-ttu-id="dcb56-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dcb56-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcb56-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="dcb56-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcb56-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dcb56-107">DESCRIPTION</span></span>
<span data-ttu-id="dcb56-108">O cmdlet **Get-AzRmStorageContainer** obtém ou lista contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcb56-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="dcb56-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcb56-109">EXAMPLES</span></span>

### <span data-ttu-id="dcb56-110">Exemplo 1: Obter um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="dcb56-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="dcb56-111">Este comando obtém um contêiner blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="dcb56-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="dcb56-112">Exemplo 2: Listar todos os contêineres de blob de armazenamento de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcb56-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="dcb56-113">Este comando lista todos os contêineres de blob de armazenamento de uma conta de armazenamento com o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dcb56-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="dcb56-114">Exemplo 3: Obter um contêiner de blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="dcb56-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="dcb56-115">Este comando obtém um contêiner blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="dcb56-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="dcb56-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dcb56-116">PARAMETERS</span></span>

### <span data-ttu-id="dcb56-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcb56-117">-AsJob</span></span>
<span data-ttu-id="dcb56-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dcb56-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcb56-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcb56-119">-DefaultProfile</span></span>
<span data-ttu-id="dcb56-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="dcb56-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcb56-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dcb56-121">-Name</span></span>
<span data-ttu-id="dcb56-122">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="dcb56-122">Container Name</span></span>

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

### <span data-ttu-id="dcb56-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcb56-123">-ResourceGroupName</span></span>
<span data-ttu-id="dcb56-124">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="dcb56-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="dcb56-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcb56-125">-StorageAccount</span></span>
<span data-ttu-id="dcb56-126">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcb56-126">Storage account object</span></span>

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

### <span data-ttu-id="dcb56-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dcb56-127">-StorageAccountName</span></span>
<span data-ttu-id="dcb56-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dcb56-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="dcb56-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcb56-129">CommonParameters</span></span>
<span data-ttu-id="dcb56-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcb56-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcb56-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcb56-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcb56-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcb56-132">INPUTS</span></span>

### <span data-ttu-id="dcb56-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dcb56-133">System.String</span></span>

### <span data-ttu-id="dcb56-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcb56-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="dcb56-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dcb56-135">OUTPUTS</span></span>

### <span data-ttu-id="dcb56-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="dcb56-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="dcb56-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="dcb56-137">NOTES</span></span>

## <span data-ttu-id="dcb56-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcb56-138">RELATED LINKS</span></span>
