---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945575"
---
# <span data-ttu-id="aa6b2-101">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="aa6b2-101">Get-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="aa6b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="aa6b2-103">Obtém mapeamentos de objetos de armazenamento de recuperação de site para um cofre.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-103">Gets mappings of Site Recovery Storage objects for a vault.</span></span>

## <span data-ttu-id="aa6b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa6b2-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aa6b2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa6b2-105">DESCRIPTION</span></span>
<span data-ttu-id="aa6b2-106">O cmdlet **Get-AzureSiteRecoveryStorageMapping** Obtém mapeamentos dos objetos de armazenamento do Azure site Recovery para o cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-106">The **Get-AzureSiteRecoveryStorageMapping** cmdlet gets mappings of Azure Site Recovery Storage objects for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="aa6b2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa6b2-107">EXAMPLES</span></span>

### <span data-ttu-id="aa6b2-108">Exemplo 1: obter o mapeamento entre um objeto de armazenamento e um objeto de armazenamento de recuperação</span><span class="sxs-lookup"><span data-stu-id="aa6b2-108">Example 1: Get the mapping between a Storage object and a recovery Storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

<span data-ttu-id="aa6b2-109">O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="aa6b2-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="aa6b2-110">O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="aa6b2-111">O segundo comando obtém o mapeamento entre dois objetos de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-111">The second command gets the mapping between two Azure Storage objects.</span></span>
<span data-ttu-id="aa6b2-112">O comando especifica o servidor primário para o mapeamento do objeto de armazenamento como o primeiro elemento de $Servers.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-112">The command specifies the primary server for the Storage object mapping as the first element of $Servers.</span></span>
<span data-ttu-id="aa6b2-113">O comando especifica o servidor para o objeto de armazenamento de recuperação como o segundo elemento de $Servers.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-113">The command specifies the server for the recovery Storage object as the second element of $Servers.</span></span>

## <span data-ttu-id="aa6b2-114">OS</span><span class="sxs-lookup"><span data-stu-id="aa6b2-114">PARAMETERS</span></span>

### <span data-ttu-id="aa6b2-115">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="aa6b2-115">-PrimaryServer</span></span>
<span data-ttu-id="aa6b2-116">Especifica o servidor primário.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-116">Specifies the primary server.</span></span>
<span data-ttu-id="aa6b2-117">Para obter um servidor, use o cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="aa6b2-117">To obtain a server, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa6b2-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="aa6b2-118">-Profile</span></span>
<span data-ttu-id="aa6b2-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aa6b2-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aa6b2-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="aa6b2-121">-RecoveryServer</span></span>
<span data-ttu-id="aa6b2-122">Especifica o servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-122">Specifies the recovery server.</span></span>
<span data-ttu-id="aa6b2-123">Para obter um servidor, use **Get-AzureSiteRecoveryServer**.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-123">To obtain a server, use **Get-AzureSiteRecoveryServer**.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa6b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa6b2-124">CommonParameters</span></span>
<span data-ttu-id="aa6b2-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa6b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa6b2-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa6b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa6b2-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa6b2-127">INPUTS</span></span>

## <span data-ttu-id="aa6b2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa6b2-128">OUTPUTS</span></span>

## <span data-ttu-id="aa6b2-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa6b2-129">NOTES</span></span>

## <span data-ttu-id="aa6b2-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa6b2-130">RELATED LINKS</span></span>

[<span data-ttu-id="aa6b2-131">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="aa6b2-131">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="aa6b2-132">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="aa6b2-132">New-AzureSiteRecoveryStorageMapping</span></span>](./New-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="aa6b2-133">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="aa6b2-133">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


