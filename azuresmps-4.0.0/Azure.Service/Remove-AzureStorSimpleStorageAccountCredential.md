---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946449"
---
# <span data-ttu-id="adc2f-101">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="adc2f-101">Remove-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="adc2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adc2f-102">SYNOPSIS</span></span>
<span data-ttu-id="adc2f-103">Exclui uma credencial de conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="adc2f-103">Deletes an existing storage account credential.</span></span>

## <span data-ttu-id="adc2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adc2f-104">SYNTAX</span></span>

### <span data-ttu-id="adc2f-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="adc2f-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="adc2f-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="adc2f-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="adc2f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adc2f-107">DESCRIPTION</span></span>
<span data-ttu-id="adc2f-108">O cmdlet **Remove-AzureStorSimpleStorageAccountCredential** exclui uma credencial de conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="adc2f-108">The **Remove-AzureStorSimpleStorageAccountCredential** cmdlet deletes an existing storage account credential.</span></span>
<span data-ttu-id="adc2f-109">Especifique uma conta por nome ou use o cmdlet **Get-AzureStorSimpleStorageAccountCredential** para obter um objeto **StorageAccountCredential** para excluir.</span><span class="sxs-lookup"><span data-stu-id="adc2f-109">Specify an account by name or use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet to obtain a **StorageAccountCredential** object to delete.</span></span>

## <span data-ttu-id="adc2f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adc2f-110">EXAMPLES</span></span>

### <span data-ttu-id="adc2f-111">Exemplo 1: remover uma credencial de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="adc2f-111">Example 1: Remove a storage account credential</span></span>
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

<span data-ttu-id="adc2f-112">Esse comando Remove a credencial da conta de armazenamento chamada ContosoStorage07.</span><span class="sxs-lookup"><span data-stu-id="adc2f-112">This command removes the account credential for the storage account named ContosoStorage07.</span></span>
<span data-ttu-id="adc2f-113">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="adc2f-113">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="adc2f-114">O cmdlet Remove a credencial sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="adc2f-114">The cmdlet removes the credential without prompting your for confirmation.</span></span>

### <span data-ttu-id="adc2f-115">Exemplo 2: remover uma credencial de conta de armazenamento usando o operador pipeline</span><span class="sxs-lookup"><span data-stu-id="adc2f-115">Example 2: Remove a storage account credential by using the pipeline operator</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

<span data-ttu-id="adc2f-116">Esse comando obtém a conta de armazenamento chamada ContosoStorage07 usando o cmdlet **Get-AzureStorSimpleStorageAccountCredential** e, em seguida, passa o objeto para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="adc2f-116">This command gets the storage account named ContosoStorage07 by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet, and then passes that object to the current cmdlet.</span></span>
<span data-ttu-id="adc2f-117">O cmdlet atual remove a credencial da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="adc2f-117">The current cmdlet removes the credential for that storage account.</span></span>
<span data-ttu-id="adc2f-118">Esse comando especifica o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="adc2f-118">This command specifies the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="adc2f-119">O cmdlet não retorna o controle para o console até que ele conclua a operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="adc2f-119">The cmdlet does not return control to the console until it completes the remove operation.</span></span>

## <span data-ttu-id="adc2f-120">OS</span><span class="sxs-lookup"><span data-stu-id="adc2f-120">PARAMETERS</span></span>

### <span data-ttu-id="adc2f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="adc2f-121">-Force</span></span>
<span data-ttu-id="adc2f-122">Indica que esse cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="adc2f-122">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="adc2f-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="adc2f-123">-Profile</span></span>
<span data-ttu-id="adc2f-124">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="adc2f-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="adc2f-125">-SAC</span><span class="sxs-lookup"><span data-stu-id="adc2f-125">-SAC</span></span>
<span data-ttu-id="adc2f-126">Especifica a credencial, como um objeto **StorageAccountCredential** , a ser removida.</span><span class="sxs-lookup"><span data-stu-id="adc2f-126">Specifies credential, as a **StorageAccountCredential** object, to remove.</span></span>
<span data-ttu-id="adc2f-127">Para obter um objeto **StorageAccountCredential** , use o cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="adc2f-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adc2f-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="adc2f-128">-StorageAccountName</span></span>
<span data-ttu-id="adc2f-129">Especifica o nome da credencial da conta de armazenamento a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="adc2f-129">Specifies the name of the storage account credential to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc2f-130">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="adc2f-130">-WaitForComplete</span></span>
<span data-ttu-id="adc2f-131">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="adc2f-131">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="adc2f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc2f-132">CommonParameters</span></span>
<span data-ttu-id="adc2f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc2f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc2f-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adc2f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc2f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adc2f-135">INPUTS</span></span>

### <span data-ttu-id="adc2f-136">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="adc2f-136">StorageAccountCredential</span></span>
<span data-ttu-id="adc2f-137">Esse cmdlet aceita um objeto **StorageAccountCredential** usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="adc2f-137">This cmdlet accepts a **StorageAccountCredential** object by using the pipeline.</span></span>

## <span data-ttu-id="adc2f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adc2f-138">OUTPUTS</span></span>

### <span data-ttu-id="adc2f-139">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="adc2f-139">TaskStatusInfo</span></span>
<span data-ttu-id="adc2f-140">Esse cmdlet retorna um objeto **TaskStatusInfo** , se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="adc2f-140">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="adc2f-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adc2f-141">NOTES</span></span>

## <span data-ttu-id="adc2f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adc2f-142">RELATED LINKS</span></span>

[<span data-ttu-id="adc2f-143">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="adc2f-143">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="adc2f-144">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="adc2f-144">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="adc2f-145">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="adc2f-145">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="adc2f-146">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="adc2f-146">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


