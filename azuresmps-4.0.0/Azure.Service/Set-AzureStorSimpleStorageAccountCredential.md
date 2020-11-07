---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 74088389-A003-4746-8A57-2146BBA7535C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0b86da15e81fd6eca005e04fc36b5887691af4bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945851"
---
# <span data-ttu-id="b1d07-101">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b1d07-101">Set-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="b1d07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1d07-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d07-103">Atualiza uma credencial de acesso de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1d07-103">Updates an Azure storage access credential.</span></span>

## <span data-ttu-id="b1d07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1d07-104">SYNTAX</span></span>

```
Set-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-StorageAccountKey <String>]
 [-UseSSL <Boolean>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b1d07-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1d07-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d07-106">O cmdlet **set-AzureStorSimpleStorageAccountCredential** atualiza uma credencial de acesso de armazenamento do Azure existente para uso por cmdlets do StorSimple OneSDK.</span><span class="sxs-lookup"><span data-stu-id="b1d07-106">The **Set-AzureStorSimpleStorageAccountCredential** cmdlet update an existing Azure storage access credential for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="b1d07-107">Para obter mais informações sobre como os cmdlets do StorSimple funcionam com contas de armazenamento, consulte o tópico da ajuda para o cmdlet New-AzureStorSimpleStorageAccountCredential.</span><span class="sxs-lookup"><span data-stu-id="b1d07-107">For more information about how StorSimple cmdlets work with storage accounts, see the help topic for the New-AzureStorSimpleStorageAccountCredential cmdlet.</span></span>

## <span data-ttu-id="b1d07-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1d07-108">EXAMPLES</span></span>

### <span data-ttu-id="b1d07-109">Exemplo 1: modificar uma credencial</span><span class="sxs-lookup"><span data-stu-id="b1d07-109">Example 1: Modify a credential</span></span>
```
PS C:\>Set-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage01" -UseSSL $False -StorageAccountKey "h9ldH4LlHJB3GujcNwgdxJACy1DaQ1Hak1bfoUBzrDqZ5DPK8+0XGbsgD+jrKfQy5PBepKpYobMViLaOC2XMdg==" -Force -WaitForComplete
VERBOSE: ClientRequestId: 20cd2b17-9cff-4ab4-a034-96d60d946295_PS
VERBOSE: ClientRequestId: a75ed193-1da5-491f-96f5-572b5461d466_PS
VERBOSE: ClientRequestId: db612c9e-e89a-404f-8406-e66e7f697cd5_PS
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: About to run a task to update your Storage Access credential! 
VERBOSE: ClientRequestId: a0995bb7-8223-4fcf-83c9-0a4f81e6a85c_PS


JobId        : 74a6172e-d47a-4824-a7fa-3eb207a76e0b
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: de04c77b-4846-45e0-9257-df501af9d4e9_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoStorage01
Name                             : ContosoStorage01
OperationInProgress              : None
Password                         : UUejow8u6ZynMm18g59883FBVtlIX6PWh6x+v15cnnkHKEAb5queTGnGOiGa/KkOqths7F/umDz+wUUB8zzq
                                   4YCi0Dm0rqPGDC4unhxvbncf+WeCEvV7qsf3pmUFdk8o96Cgl8oXgmmvYL9K6Z6ajHUdZFFlq9WqUpz2vBbz
                                   3ROxq8SRORt2DQVQP6LWojTiow1kNI/v2cs3eNvzoSgGftqzjSmhaTYu+q0o8X07eE4KwkWhQrRX24seH2Lg
                                   N9aYCQUrSxVKOAFJjdLOIBUlM48pnE7xyyZNwqngnPLt8z+mlS6JCKfo5SBKUfwmkhgDFfbVwB3jqC/sV/G6
                                   omwQ/A==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="b1d07-110">Esse comando altera a credencial da conta de armazenamento chamada ContosoStorage01 para não exigir mais SSL.</span><span class="sxs-lookup"><span data-stu-id="b1d07-110">This command changes the storage account credential named ContosoStorage01 to no longer require SSL.</span></span>

## <span data-ttu-id="b1d07-111">OS</span><span class="sxs-lookup"><span data-stu-id="b1d07-111">PARAMETERS</span></span>

### <span data-ttu-id="b1d07-112">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b1d07-112">-Profile</span></span>
<span data-ttu-id="b1d07-113">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1d07-113">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b1d07-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b1d07-114">-StorageAccountKey</span></span>
<span data-ttu-id="b1d07-115">Especifica a tecla de acesso da conta de armazenamento em texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="b1d07-115">Specifies the access key of the storage account in plain text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d07-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1d07-116">-StorageAccountName</span></span>
<span data-ttu-id="b1d07-117">Especifica o nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="b1d07-117">Specifies the name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d07-118">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="b1d07-118">-UseSSL</span></span>
<span data-ttu-id="b1d07-119">Indica se você deve usar SSL para a conexão ao usar a nova credencial de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b1d07-119">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d07-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b1d07-120">-WaitForComplete</span></span>
<span data-ttu-id="b1d07-121">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b1d07-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="b1d07-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d07-122">CommonParameters</span></span>
<span data-ttu-id="b1d07-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1d07-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d07-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d07-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d07-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1d07-125">INPUTS</span></span>

### <span data-ttu-id="b1d07-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b1d07-126">None</span></span>

## <span data-ttu-id="b1d07-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1d07-127">OUTPUTS</span></span>

### <span data-ttu-id="b1d07-128">StorageAccountCredentialResponse, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="b1d07-128">StorageAccountCredentialResponse, TaskResponse</span></span>
<span data-ttu-id="b1d07-129">Esse cmdlet retorna um objeto **StorageAccountCredentialResponse** , se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="b1d07-129">This cmdlet returns a **StorageAccountCredentialResponse** object, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="b1d07-130">Se você não especificar esse parâmetro, o cmdlet retornará um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="b1d07-130">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="b1d07-131">Um **StorageAccountCredentialResponse** contém as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="b1d07-131">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="b1d07-132">**Cloudtype** ( **cloudtype** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-132">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="b1d07-133">**Nome do host** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-133">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="b1d07-134">**InstanceId** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-134">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="b1d07-135">**IsDefault** ( **Boolean** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-135">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="b1d07-136">**Local** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-136">**Location** ( **String** )</span></span>
- <span data-ttu-id="b1d07-137">**Login** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-137">**Login** ( **String** )</span></span>
- <span data-ttu-id="b1d07-138">**Name** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-138">**Name** ( **String** )</span></span>
- <span data-ttu-id="b1d07-139">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-139">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="b1d07-140">**Senha** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-140">**Password** ( **String** )</span></span>
- <span data-ttu-id="b1d07-141">**PasswordEncryptionCertThumbprint** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-141">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="b1d07-142">**UseSSL** ( **booliano** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-142">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="b1d07-143">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="b1d07-143">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="b1d07-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1d07-144">NOTES</span></span>

## <span data-ttu-id="b1d07-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1d07-145">RELATED LINKS</span></span>

[<span data-ttu-id="b1d07-146">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b1d07-146">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="b1d07-147">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b1d07-147">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="b1d07-148">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b1d07-148">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)


