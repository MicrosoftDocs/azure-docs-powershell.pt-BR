---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946096"
---
# <span data-ttu-id="4f239-101">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="4f239-101">Remove-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="4f239-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f239-102">SYNOPSIS</span></span>
<span data-ttu-id="4f239-103">Exclui um registro de controle de acesso da configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="4f239-103">Deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="4f239-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f239-104">SYNTAX</span></span>

### <span data-ttu-id="4f239-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="4f239-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4f239-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="4f239-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f239-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f239-107">DESCRIPTION</span></span>
<span data-ttu-id="4f239-108">O cmdlet **Remove-AzureStorSimpleAccessControlRecord** exclui um registro de controle de acesso da configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="4f239-108">The **Remove-AzureStorSimpleAccessControlRecord** cmdlet deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="4f239-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f239-109">EXAMPLES</span></span>

### <span data-ttu-id="4f239-110">Exemplo 1: remover um controle de recordaccess de controle de Controlaccess de acesso</span><span class="sxs-lookup"><span data-stu-id="4f239-110">Example 1: Remove an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

<span data-ttu-id="4f239-111">Esse comando exclui o registro de controle de acesso chamado Acr10.</span><span class="sxs-lookup"><span data-stu-id="4f239-111">This command deletes the access control record named Acr10.</span></span>
<span data-ttu-id="4f239-112">Esse comando especifica o parâmetro *WaitForComplete* e, portanto, o comando aguarda até que a operação seja concluída e, em seguida, retorna um objeto **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="4f239-112">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="4f239-113">Exemplo 2: remover um registro de controle de Controlaccess de acesso usando o controle Controlaccess Controlaccess de pipelineAccess</span><span class="sxs-lookup"><span data-stu-id="4f239-113">Example 2: Remove an Access Controlaccess control record by using the pipelineAccess Controlaccess controlaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

<span data-ttu-id="4f239-114">Esse comando usa **Get-AzureStorSimpleAccessControlRecord** para obter o **AccessControlRecord** chamado Acr10 e, em seguida, passa o objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="4f239-114">This command uses the **Get-AzureStorSimpleAccessControlRecord** to get the **AccessControlRecord** named Acr10, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4f239-115">O comando inicia a operação que remove o objeto **AccessControlRecord** e, em seguida, retorna um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="4f239-115">The command starts the operation that removes the **AccessControlRecord** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="4f239-116">Para ver o status da tarefa, use o cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="4f239-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="4f239-117">OS</span><span class="sxs-lookup"><span data-stu-id="4f239-117">PARAMETERS</span></span>

### <span data-ttu-id="4f239-118">-ACR</span><span class="sxs-lookup"><span data-stu-id="4f239-118">-ACR</span></span>
<span data-ttu-id="4f239-119">Especifica um objeto **AccessControlRecord** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4f239-119">Specifies an **AccessControlRecord** object to delete.</span></span>
<span data-ttu-id="4f239-120">Para obter um objeto **AccessControlRecord** , use o cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="4f239-120">To obtain an **AccessControlRecord** object, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f239-121">-ACRName</span><span class="sxs-lookup"><span data-stu-id="4f239-121">-ACRName</span></span>
<span data-ttu-id="4f239-122">Especifica um nome do registro de controle de acesso a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4f239-122">Specifies a name of the access control record to delete.</span></span>

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

### <span data-ttu-id="4f239-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4f239-123">-Force</span></span>
<span data-ttu-id="4f239-124">Indica que esse cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="4f239-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="4f239-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4f239-125">-Profile</span></span>
<span data-ttu-id="4f239-126">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f239-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="4f239-127">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="4f239-127">-WaitForComplete</span></span>
<span data-ttu-id="4f239-128">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f239-128">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="4f239-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f239-129">CommonParameters</span></span>
<span data-ttu-id="4f239-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f239-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f239-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f239-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f239-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f239-132">INPUTS</span></span>

### <span data-ttu-id="4f239-133">AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="4f239-133">AccessControlRecord</span></span>
<span data-ttu-id="4f239-134">Esse cmdlet aceita um objeto **AccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="4f239-134">This cmdlet accepts an **AccessControlRecord** object.</span></span>
<span data-ttu-id="4f239-135">Um objeto **AccessControlRecord** contém os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="4f239-135">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="4f239-136">**GlobalId** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="4f239-136">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="4f239-137">**Initiatorname** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="4f239-137">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="4f239-138">**InstanceId** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="4f239-138">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="4f239-139">**Name** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="4f239-139">**Name** ( **String** )</span></span> 
- <span data-ttu-id="4f239-140">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="4f239-140">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="4f239-141">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="4f239-141">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="4f239-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f239-142">OUTPUTS</span></span>

### <span data-ttu-id="4f239-143">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="4f239-143">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="4f239-144">Esse cmdlet retorna um objeto **TaskStatusInfo** se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="4f239-144">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="4f239-145">Se você não especificar esse parâmetro, ele retornará um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="4f239-145">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="4f239-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f239-146">NOTES</span></span>

## <span data-ttu-id="4f239-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f239-147">RELATED LINKS</span></span>

[<span data-ttu-id="4f239-148">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="4f239-148">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="4f239-149">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="4f239-149">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="4f239-150">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="4f239-150">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="4f239-151">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="4f239-151">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


