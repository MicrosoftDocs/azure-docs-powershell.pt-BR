---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946210"
---
# <span data-ttu-id="7f0a6-101">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="7f0a6-101">New-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="7f0a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0a6-103">Cria um registro de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="7f0a6-103">Creates an access control record.</span></span>

## <span data-ttu-id="7f0a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f0a6-104">SYNTAX</span></span>

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7f0a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f0a6-105">DESCRIPTION</span></span>
<span data-ttu-id="7f0a6-106">O cmdlet **New-AzureStorSimpleAccessControlRecord** cria um registro de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="7f0a6-106">The **New-AzureStorSimpleAccessControlRecord** cmdlet creates an access control record.</span></span>
<span data-ttu-id="7f0a6-107">Você pode usar um objeto **AccessControlRecord** para configurar volumes.</span><span class="sxs-lookup"><span data-stu-id="7f0a6-107">You can use an **AccessControlRecord** object to configure volumes.</span></span>

## <span data-ttu-id="7f0a6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f0a6-108">EXAMPLES</span></span>

### <span data-ttu-id="7f0a6-109">Exemplo 1: criar um registro de controle Controlaccess do Access e esperar o controle resultaccess</span><span class="sxs-lookup"><span data-stu-id="7f0a6-109">Example 1: Create an Access Controlaccess control record and wait for the resultaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

<span data-ttu-id="7f0a6-110">Esse comando cria um registro de controle de acesso chamado Acr10 para o iniciador iSCSI chamado Iqn10.</span><span class="sxs-lookup"><span data-stu-id="7f0a6-110">This command creates an access control record named Acr10 for the iSCSI initiator named Iqn10.</span></span>
<span data-ttu-id="7f0a6-111">Esse comando especifica o parâmetro *WaitForComplete* e, portanto, o comando aguarda até que a operação seja concluída e, em seguida, retorna um objeto **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="7f0a6-111">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="7f0a6-112">Exemplo 2: criar um controle de recordaccess de controle de Controlaccess de acesso</span><span class="sxs-lookup"><span data-stu-id="7f0a6-112">Example 2: Create an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

<span data-ttu-id="7f0a6-113">Esse comando cria um registro de controle de acesso chamado Acr11 para o iniciador iSCSI chamado Iqn11.</span><span class="sxs-lookup"><span data-stu-id="7f0a6-113">This command creates an access control record named Acr11 for the iSCSI initiator named Iqn11.</span></span>
<span data-ttu-id="7f0a6-114">Esse comando não especifica o parâmetro *WaitForComplete* e, portanto, o comando inicia a tarefa e, em seguida, retorna um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="7f0a6-114">This command does not specify the *WaitForComplete* parameter, and, therefore, the command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="7f0a6-115">Para ver o status da tarefa, use o cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="7f0a6-115">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="7f0a6-116">OS</span><span class="sxs-lookup"><span data-stu-id="7f0a6-116">PARAMETERS</span></span>

### <span data-ttu-id="7f0a6-117">-ACRName</span><span class="sxs-lookup"><span data-stu-id="7f0a6-117">-ACRName</span></span>
<span data-ttu-id="7f0a6-118">Especifica um nome para o registro de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="7f0a6-118">Specifies a name for the access control record.</span></span>

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

### <span data-ttu-id="7f0a6-119">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="7f0a6-119">-IQNInitiatorName</span></span>
<span data-ttu-id="7f0a6-120">Especifica o nome qualificado iSCSI (IQN) do iniciador iSCSI ao qual esse cmdlet fornece acesso para o volume.</span><span class="sxs-lookup"><span data-stu-id="7f0a6-120">Specifies the iSCSI qualified name (IQN) of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0a6-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7f0a6-121">-Profile</span></span>
<span data-ttu-id="7f0a6-122">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f0a6-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7f0a6-123">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="7f0a6-123">-WaitForComplete</span></span>
<span data-ttu-id="7f0a6-124">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7f0a6-124">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7f0a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0a6-125">CommonParameters</span></span>
<span data-ttu-id="7f0a6-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f0a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0a6-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f0a6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0a6-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f0a6-128">INPUTS</span></span>

### <span data-ttu-id="7f0a6-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7f0a6-129">None</span></span>

## <span data-ttu-id="7f0a6-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f0a6-130">OUTPUTS</span></span>

### <span data-ttu-id="7f0a6-131">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="7f0a6-131">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="7f0a6-132">Esse cmdlet retorna um objeto **TaskStatusInfo** se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="7f0a6-132">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="7f0a6-133">Se você não especificar esse parâmetro, ele retornará um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="7f0a6-133">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="7f0a6-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f0a6-134">NOTES</span></span>

## <span data-ttu-id="7f0a6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f0a6-135">RELATED LINKS</span></span>

[<span data-ttu-id="7f0a6-136">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="7f0a6-136">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="7f0a6-137">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="7f0a6-137">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="7f0a6-138">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="7f0a6-138">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="7f0a6-139">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="7f0a6-139">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


