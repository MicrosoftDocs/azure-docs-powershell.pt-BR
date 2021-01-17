---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: cdc2f8b1742625feb042865a9b75e2c495d7aac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427879"
---
# <span data-ttu-id="ffa6c-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ffa6c-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="ffa6c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffa6c-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa6c-103">Obter ou listar escopos de criptografia de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ffa6c-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="ffa6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffa6c-104">SYNTAX</span></span>

### <span data-ttu-id="ffa6c-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ffa6c-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffa6c-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="ffa6c-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffa6c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffa6c-107">DESCRIPTION</span></span>
<span data-ttu-id="ffa6c-108">O cmdlet **Get-AzStorageEncryptionScope** Obtém ou lista escopos de criptografia de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ffa6c-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="ffa6c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffa6c-109">EXAMPLES</span></span>

### <span data-ttu-id="ffa6c-110">Exemplo 1: obter um único escopo de criptografia</span><span class="sxs-lookup"><span data-stu-id="ffa6c-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="ffa6c-111">Esse comando obtém um único escopo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="ffa6c-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="ffa6c-112">Exemplo 2: listar todos os escopos de criptografia de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ffa6c-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="ffa6c-113">Esse comando lista todos os escopos de criptografia de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ffa6c-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="ffa6c-114">OS</span><span class="sxs-lookup"><span data-stu-id="ffa6c-114">PARAMETERS</span></span>

### <span data-ttu-id="ffa6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa6c-115">-DefaultProfile</span></span>
<span data-ttu-id="ffa6c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa6c-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="ffa6c-117">-EncryptionScopeName</span></span>
<span data-ttu-id="ffa6c-118">Nome do EncryptionScope de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="ffa6c-118">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa6c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa6c-119">-ResourceGroupName</span></span>
<span data-ttu-id="ffa6c-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ffa6c-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa6c-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ffa6c-121">-StorageAccount</span></span>
<span data-ttu-id="ffa6c-122">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ffa6c-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa6c-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ffa6c-123">-StorageAccountName</span></span>
<span data-ttu-id="ffa6c-124">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ffa6c-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa6c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa6c-125">CommonParameters</span></span>
<span data-ttu-id="ffa6c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa6c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa6c-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa6c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa6c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffa6c-128">INPUTS</span></span>

### <span data-ttu-id="ffa6c-129">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ffa6c-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ffa6c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffa6c-130">OUTPUTS</span></span>

### <span data-ttu-id="ffa6c-131">Microsoft. Azure. Commands. Management. Storage. Models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ffa6c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="ffa6c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffa6c-132">NOTES</span></span>

## <span data-ttu-id="ffa6c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffa6c-133">RELATED LINKS</span></span>
