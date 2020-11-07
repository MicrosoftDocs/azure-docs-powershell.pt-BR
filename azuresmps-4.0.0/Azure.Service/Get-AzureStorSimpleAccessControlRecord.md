---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946552"
---
# <span data-ttu-id="22717-101">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="22717-101">Get-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="22717-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22717-102">SYNOPSIS</span></span>
<span data-ttu-id="22717-103">Obtém registros de controle de acesso em uma configuração de serviço.</span><span class="sxs-lookup"><span data-stu-id="22717-103">Gets access control records in a service configuration.</span></span>

## <span data-ttu-id="22717-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22717-104">SYNTAX</span></span>

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="22717-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22717-105">DESCRIPTION</span></span>
<span data-ttu-id="22717-106">O cmdlet **Get-AzureStorSimpleAccessControlRecord** Obtém registros de controle de acesso na configuração do serviço StorSimple Manager.</span><span class="sxs-lookup"><span data-stu-id="22717-106">The **Get-AzureStorSimpleAccessControlRecord** cmdlet gets access control records in the StorSimple Manager service configuration.</span></span>
<span data-ttu-id="22717-107">Este cmdlet obtém todos os registros ou um registro nomeado.</span><span class="sxs-lookup"><span data-stu-id="22717-107">This cmdlet gets all records or a named record.</span></span>

<span data-ttu-id="22717-108">Os registros de controle de acesso são recipientes de parâmetros do iniciador iSCSI.</span><span class="sxs-lookup"><span data-stu-id="22717-108">Access control records are containers of iSCSI initiator parameters.</span></span>
<span data-ttu-id="22717-109">Esses parâmetros especificam quais iniciadores podem acessar um volume.</span><span class="sxs-lookup"><span data-stu-id="22717-109">These parameters specify which initiators can access a volume.</span></span>
<span data-ttu-id="22717-110">Quando um iniciador iSCSI tenta se conectar a um volume, seu aparelho verifica os registros de controle de acesso atribuídos a esse volume.</span><span class="sxs-lookup"><span data-stu-id="22717-110">When an iSCSI initiator attempts to connect to a volume, your appliance checks the access control records assigned to that volume.</span></span>
<span data-ttu-id="22717-111">Se os parâmetros do iniciador iSCSI corresponderem a uma das entradas em um registro de controle de acesso mapeado para esse volume, o iniciador iSCSI poderá se conectar.</span><span class="sxs-lookup"><span data-stu-id="22717-111">If the iSCSI initiator parameters match one of the entries in an access control record mapped to that volume, the iSCSI initiator can connect.</span></span>

## <span data-ttu-id="22717-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22717-112">EXAMPLES</span></span>

### <span data-ttu-id="22717-113">Exemplo 1: obter todos os registros de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="22717-113">Example 1: Get all access control records</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

<span data-ttu-id="22717-114">Esse comando obtém todos os registros de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="22717-114">This command gets all access control records.</span></span>

### <span data-ttu-id="22717-115">Exemplo 2: obter um registro de controle de acesso específico</span><span class="sxs-lookup"><span data-stu-id="22717-115">Example 2: Get a specific access control record</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

<span data-ttu-id="22717-116">Esse comando obtém o registro de controle de acesso chamado Acr11.</span><span class="sxs-lookup"><span data-stu-id="22717-116">This command gets the access control record named Acr11.</span></span>

## <span data-ttu-id="22717-117">OS</span><span class="sxs-lookup"><span data-stu-id="22717-117">PARAMETERS</span></span>

### <span data-ttu-id="22717-118">-ACRName</span><span class="sxs-lookup"><span data-stu-id="22717-118">-ACRName</span></span>
<span data-ttu-id="22717-119">Especifica o nome de um registro de controle de acesso a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="22717-119">Specifies the name of an access control record to get.</span></span>

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

### <span data-ttu-id="22717-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="22717-120">-Profile</span></span>
<span data-ttu-id="22717-121">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="22717-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="22717-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22717-122">CommonParameters</span></span>
<span data-ttu-id="22717-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22717-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22717-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22717-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22717-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22717-125">INPUTS</span></span>

### <span data-ttu-id="22717-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="22717-126">None</span></span>

## <span data-ttu-id="22717-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22717-127">OUTPUTS</span></span>

### <span data-ttu-id="22717-128">AccessControlRecord, IList\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="22717-128">AccessControlRecord, IList\<AccessControlRecord\></span></span>
<span data-ttu-id="22717-129">Esse cmdlet retorna um objeto **AccessControlRecord** ou um **objeto \<AccessControlRecord\> IList** .</span><span class="sxs-lookup"><span data-stu-id="22717-129">This cmdlet returns an **AccessControlRecord** object or an **IList\<AccessControlRecord\>** object.</span></span>
<span data-ttu-id="22717-130">Um objeto **AccessControlRecord** contém os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="22717-130">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="22717-131">**GlobalId** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="22717-131">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="22717-132">**Initiatorname** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="22717-132">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="22717-133">**InstanceId** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="22717-133">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="22717-134">**Name** ( **cadeia** )</span><span class="sxs-lookup"><span data-stu-id="22717-134">**Name** ( **String** )</span></span> 
- <span data-ttu-id="22717-135">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="22717-135">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="22717-136">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="22717-136">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="22717-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22717-137">NOTES</span></span>

## <span data-ttu-id="22717-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22717-138">RELATED LINKS</span></span>

[<span data-ttu-id="22717-139">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="22717-139">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="22717-140">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="22717-140">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="22717-141">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="22717-141">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)


