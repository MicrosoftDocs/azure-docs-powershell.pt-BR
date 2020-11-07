---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71CFCA9D-198E-481A-BB85-159477F25322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c050ea91cc85a89702fb6cf62f05779db7155e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945858"
---
# <span data-ttu-id="ca4af-101">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ca4af-101">Set-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="ca4af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca4af-102">SYNOPSIS</span></span>
<span data-ttu-id="ca4af-103">Atualiza o IQN de um registro de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="ca4af-103">Updates the IQN of an access control record.</span></span>

## <span data-ttu-id="ca4af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca4af-104">SYNTAX</span></span>

```
Set-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ca4af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca4af-105">DESCRIPTION</span></span>
<span data-ttu-id="ca4af-106">O cmdlet **set-AzureStorSimpleAccessControlRecord** atualiza o nome qualificado iSCSI (iqn) de um registro de controle de acesso existente.</span><span class="sxs-lookup"><span data-stu-id="ca4af-106">The **Set-AzureStorSimpleAccessControlRecord** cmdlet updates the iSCSI qualified name (IQN) of an existing access control record.</span></span>

## <span data-ttu-id="ca4af-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca4af-107">EXAMPLES</span></span>

### <span data-ttu-id="ca4af-108">Exemplo 1: atualizar um registro de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="ca4af-108">Example 1: Update an access control record</span></span>
```
PS C:\>Set-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "IqnUpdated" -WaitForComplete
VERBOSE: ClientRequestId: e4766335-f302-40e0-93bf-fad7aa488ae6_PS
VERBOSE: ClientRequestId: cfdbbd67-6ba5-4238-b743-b88f604079b9_PS
VERBOSE: About to run a task to update your Access Control Record! 
VERBOSE: ClientRequestId: d5cf2793-0ab5-40ff-ab6f-43e21bc4c0a4_PS


JobId        : 89502523-52fc-4ce2-b2d4-cb8c6692fb60
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: cbd47519-3a3c-4365-b097-0fb7551c48ee_PS
GlobalId            : 
InitiatorName       : IqnUpdated
InstanceId          : 9bcfbc83-e196-4688-9016-827f51515c24
Name                : Acr10
OperationInProgress : None
VolumeCount         : 0
```

<span data-ttu-id="ca4af-109">Esse comando atualiza o registro de controle de acesso chamado Acr10 para o iniciador iSCSI chamado IqnUpdated.</span><span class="sxs-lookup"><span data-stu-id="ca4af-109">This command updates the access control record named Acr10 for the iSCSI initiator named IqnUpdated.</span></span>
<span data-ttu-id="ca4af-110">Esse comando especifica o parâmetro *WaitForComplete* e, portanto, o comando aguarda até que a operação seja concluída e, em seguida, retorna um objeto **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="ca4af-110">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="ca4af-111">OS</span><span class="sxs-lookup"><span data-stu-id="ca4af-111">PARAMETERS</span></span>

### <span data-ttu-id="ca4af-112">-ACRName</span><span class="sxs-lookup"><span data-stu-id="ca4af-112">-ACRName</span></span>
<span data-ttu-id="ca4af-113">Especifica um nome do registro de controle de acesso a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ca4af-113">Specifies a name of the access control record to modify.</span></span>

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

### <span data-ttu-id="ca4af-114">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="ca4af-114">-IQNInitiatorName</span></span>
<span data-ttu-id="ca4af-115">Especifica o IQN do iniciador iSCSI para o qual esse cmdlet fornece acesso para o volume.</span><span class="sxs-lookup"><span data-stu-id="ca4af-115">Specifies the IQN of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

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

### <span data-ttu-id="ca4af-116">-NewName</span><span class="sxs-lookup"><span data-stu-id="ca4af-116">-NewName</span></span>
<span data-ttu-id="ca4af-117">Especifica um novo nome para o registro de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="ca4af-117">Specifies a new name for access control record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4af-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ca4af-118">-Profile</span></span>
<span data-ttu-id="ca4af-119">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca4af-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ca4af-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="ca4af-120">-WaitForComplete</span></span>
<span data-ttu-id="ca4af-121">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca4af-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ca4af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca4af-122">CommonParameters</span></span>
<span data-ttu-id="ca4af-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca4af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca4af-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca4af-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca4af-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca4af-125">INPUTS</span></span>

### <span data-ttu-id="ca4af-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ca4af-126">None</span></span>

## <span data-ttu-id="ca4af-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca4af-127">OUTPUTS</span></span>

### <span data-ttu-id="ca4af-128">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="ca4af-128">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="ca4af-129">Esse cmdlet retorna um objeto **TaskStatusInfo** se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="ca4af-129">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="ca4af-130">Se você não especificar esse parâmetro, ele retornará um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="ca4af-130">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="ca4af-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca4af-131">NOTES</span></span>

## <span data-ttu-id="ca4af-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca4af-132">RELATED LINKS</span></span>

[<span data-ttu-id="ca4af-133">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ca4af-133">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="ca4af-134">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ca4af-134">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="ca4af-135">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ca4af-135">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)


