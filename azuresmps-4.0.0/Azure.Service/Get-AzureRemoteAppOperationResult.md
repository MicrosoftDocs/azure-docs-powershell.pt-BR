---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946322"
---
# <span data-ttu-id="19ddc-101">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="19ddc-101">Get-AzureRemoteAppOperationResult</span></span>

## <span data-ttu-id="19ddc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="19ddc-103">Recupera o resultado de uma operação do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="19ddc-103">Retrieves the result of an Azure RemoteApp operation.</span></span>

## <span data-ttu-id="19ddc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19ddc-104">SYNTAX</span></span>

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="19ddc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19ddc-105">DESCRIPTION</span></span>
<span data-ttu-id="19ddc-106">O cmdlet **Get-AzureRemoteAppOperationResult** recupera o resultado de uma operação de tempo de execução do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="19ddc-106">The **Get-AzureRemoteAppOperationResult** cmdlet retrieves the result of a long-running Azure RemoteApp operation.</span></span>
<span data-ttu-id="19ddc-107">O Azure RemoteApp usa operações de longa duração para várias ações que exigem processamento pelo serviço e não podem retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="19ddc-107">Azure RemoteApp uses long-running operations for many actions that require processing by the service and cannot return immediately.</span></span>
<span data-ttu-id="19ddc-108">Exemplos de cmdlets que retornam as IDs de rastreamento incluem **Update-AzureRemoteAppCollection** , **set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** e outros.</span><span class="sxs-lookup"><span data-stu-id="19ddc-108">Examples of cmdlets that return tracking IDs include **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** , and others.</span></span>

## <span data-ttu-id="19ddc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19ddc-109">EXAMPLES</span></span>

### <span data-ttu-id="19ddc-110">Exemplo 1: usar uma ID de rastreamento para obter um resultado de operação</span><span class="sxs-lookup"><span data-stu-id="19ddc-110">Example 1: Use a tracking ID to get an operation result</span></span>
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

<span data-ttu-id="19ddc-111">Esse comando salva a ID de rastreamento retornada de uma operação do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="19ddc-111">This command saves the tracking ID returned from an Azure RemoteApp operation.</span></span>
<span data-ttu-id="19ddc-112">A ID de rastreamento é passada para **Get-AzureRemoteAppOperationResult** no comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="19ddc-112">The tracking ID is passed to **Get-AzureRemoteAppOperationResult** in the command that follows.</span></span>

## <span data-ttu-id="19ddc-113">OS</span><span class="sxs-lookup"><span data-stu-id="19ddc-113">PARAMETERS</span></span>

### <span data-ttu-id="19ddc-114">-Perfil</span><span class="sxs-lookup"><span data-stu-id="19ddc-114">-Profile</span></span>
<span data-ttu-id="19ddc-115">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="19ddc-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19ddc-116">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="19ddc-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19ddc-117">-TrackingID</span><span class="sxs-lookup"><span data-stu-id="19ddc-117">-TrackingId</span></span>
<span data-ttu-id="19ddc-118">Especifica a ID de rastreamento de uma operação.</span><span class="sxs-lookup"><span data-stu-id="19ddc-118">Specifies the tracking ID of an operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19ddc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ddc-119">CommonParameters</span></span>
<span data-ttu-id="19ddc-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19ddc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ddc-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19ddc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ddc-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19ddc-122">INPUTS</span></span>

## <span data-ttu-id="19ddc-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19ddc-123">OUTPUTS</span></span>

## <span data-ttu-id="19ddc-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19ddc-124">NOTES</span></span>

## <span data-ttu-id="19ddc-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19ddc-125">RELATED LINKS</span></span>

[<span data-ttu-id="19ddc-126">Desconectar-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="19ddc-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="19ddc-127">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="19ddc-127">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)

[<span data-ttu-id="19ddc-128">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="19ddc-128">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


