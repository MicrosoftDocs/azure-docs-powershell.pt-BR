---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945551"
---
# <span data-ttu-id="3e8b5-101">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3e8b5-101">Get-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="3e8b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8b5-103">Obtém credenciais para contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3e8b5-103">Gets credentials for storage accounts.</span></span>

## <span data-ttu-id="3e8b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e8b5-104">SYNTAX</span></span>

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e8b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e8b5-105">DESCRIPTION</span></span>
<span data-ttu-id="3e8b5-106">O cmdlet **Get-AzureStorSimpleStorageAccountCredential** Obtém credenciais para contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3e8b5-106">The **Get-AzureStorSimpleStorageAccountCredential** cmdlet gets credentials for storage accounts.</span></span>
<span data-ttu-id="3e8b5-107">Esse cmdlet obtém todos os objetos **StorageAccountCredential** configurados no serviço ou em um chamado **StorageAccountCredential**.</span><span class="sxs-lookup"><span data-stu-id="3e8b5-107">This cmdlet gets all **StorageAccountCredential** objects configured in the service or a named **StorageAccountCredential**.</span></span>

## <span data-ttu-id="3e8b5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e8b5-108">EXAMPLES</span></span>

### <span data-ttu-id="3e8b5-109">Exemplo 1: obter todas as credenciais para um recurso</span><span class="sxs-lookup"><span data-stu-id="3e8b5-109">Example 1: Get all credentials for a resource</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

<span data-ttu-id="3e8b5-110">Este comando obtém todas as credenciais disponíveis para contas de armazenamento do recurso atual.</span><span class="sxs-lookup"><span data-stu-id="3e8b5-110">This command gets all available credentials for storage accounts for the current resource.</span></span>

### <span data-ttu-id="3e8b5-111">Exemplo 2: obter a credencial para uma conta de armazenamento específica</span><span class="sxs-lookup"><span data-stu-id="3e8b5-111">Example 2: Get the credential for a specific storage account</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

<span data-ttu-id="3e8b5-112">Este comando obtém a credencial da conta de armazenamento da conta de armazenamento chamada ContosoCloudStorage.</span><span class="sxs-lookup"><span data-stu-id="3e8b5-112">This command gets the storage account credential for the storage account named ContosoCloudStorage.</span></span>

## <span data-ttu-id="3e8b5-113">OS</span><span class="sxs-lookup"><span data-stu-id="3e8b5-113">PARAMETERS</span></span>

### <span data-ttu-id="3e8b5-114">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3e8b5-114">-Profile</span></span>
<span data-ttu-id="3e8b5-115">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8b5-115">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8b5-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e8b5-116">-StorageAccountName</span></span>
<span data-ttu-id="3e8b5-117">Especifica o nome da conta de armazenamento para a qual obter as credenciais.</span><span class="sxs-lookup"><span data-stu-id="3e8b5-117">Specifies the name of the storage account for which to get credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8b5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8b5-118">CommonParameters</span></span>
<span data-ttu-id="3e8b5-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e8b5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8b5-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e8b5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8b5-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e8b5-121">INPUTS</span></span>

### <span data-ttu-id="3e8b5-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3e8b5-122">None</span></span>

## <span data-ttu-id="3e8b5-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e8b5-123">OUTPUTS</span></span>

### <span data-ttu-id="3e8b5-124">StorageAccountCredential, IList\<StorageAccountCredential\></span><span class="sxs-lookup"><span data-stu-id="3e8b5-124">StorageAccountCredential, IList\<StorageAccountCredential\></span></span>
<span data-ttu-id="3e8b5-125">Esse cmdlet retorna um objeto **StorageAccountCredential** , se você especificar o parâmetro *StorageAccountName* ou se você não especificar esse parâmetro, ele retornará um objeto **IList \<StorageAccountCredential\>** .</span><span class="sxs-lookup"><span data-stu-id="3e8b5-125">This cmdlet returns a **StorageAccountCredential** object, if you specify the *StorageAccountName* parameter, or if you do not specify that parameter, it returns an **IList\<StorageAccountCredential\>** object.</span></span>

## <span data-ttu-id="3e8b5-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e8b5-126">NOTES</span></span>

## <span data-ttu-id="3e8b5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e8b5-127">RELATED LINKS</span></span>

[<span data-ttu-id="3e8b5-128">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3e8b5-128">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="3e8b5-129">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3e8b5-129">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="3e8b5-130">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3e8b5-130">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)


