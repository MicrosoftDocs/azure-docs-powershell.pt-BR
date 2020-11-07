---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946109"
---
# <span data-ttu-id="50899-101">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="50899-101">Remove-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="50899-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50899-102">SYNOPSIS</span></span>
<span data-ttu-id="50899-103">Remove um mapeamento de objeto de armazenamento para um cofre de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="50899-103">Removes a Storage object mapping for a Site Recovery vault.</span></span>

## <span data-ttu-id="50899-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50899-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="50899-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50899-105">DESCRIPTION</span></span>
<span data-ttu-id="50899-106">O cmdlet **Remove-AzureSiteRecoveryStorageMapping** remove um mapeamento de objeto de armazenamento do cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="50899-106">The **Remove-AzureSiteRecoveryStorageMapping** cmdlet removes a Storage object mapping for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="50899-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50899-107">EXAMPLES</span></span>

### <span data-ttu-id="50899-108">Exemplo 1: remover o mapeamento entre uma rede e uma rede de recuperação</span><span class="sxs-lookup"><span data-stu-id="50899-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

<span data-ttu-id="50899-109">O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="50899-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="50899-110">O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="50899-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="50899-111">O segundo comando obtém o mapeamento entre dois objetos de armazenamento e, em seguida, armazena-o na variável $StorageMapping.</span><span class="sxs-lookup"><span data-stu-id="50899-111">The second command gets the mapping between two Storage objects, and then stores it in the $StorageMapping variable.</span></span>
<span data-ttu-id="50899-112">O comando especifica o servidor primário para o mapeamento de rede como o primeiro elemento de $Servers.</span><span class="sxs-lookup"><span data-stu-id="50899-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="50899-113">O comando especifica o servidor para a rede de recuperação como o segundo elemento de $Servers.</span><span class="sxs-lookup"><span data-stu-id="50899-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="50899-114">O comando final remove o mapeamento em $StorageMapping.</span><span class="sxs-lookup"><span data-stu-id="50899-114">The final command removes the mapping in $StorageMapping.</span></span>

## <span data-ttu-id="50899-115">OS</span><span class="sxs-lookup"><span data-stu-id="50899-115">PARAMETERS</span></span>

### <span data-ttu-id="50899-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="50899-116">-Profile</span></span>
<span data-ttu-id="50899-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="50899-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50899-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="50899-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50899-119">-StorageMapping</span><span class="sxs-lookup"><span data-stu-id="50899-119">-StorageMapping</span></span>
<span data-ttu-id="50899-120">Especifica um mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="50899-120">Specifies a network mapping.</span></span>
<span data-ttu-id="50899-121">Para obter um **ASRStorageMapping** , use o cmdlet **Get-AzureSiteRecoveryStorage** .</span><span class="sxs-lookup"><span data-stu-id="50899-121">To obtain an **ASRStorageMapping** , use the **Get-AzureSiteRecoveryStorage** cmdlet.</span></span>

```yaml
Type: ASRStorageMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50899-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50899-122">CommonParameters</span></span>
<span data-ttu-id="50899-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50899-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50899-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50899-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50899-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50899-125">INPUTS</span></span>

## <span data-ttu-id="50899-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50899-126">OUTPUTS</span></span>

## <span data-ttu-id="50899-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50899-127">NOTES</span></span>

## <span data-ttu-id="50899-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50899-128">RELATED LINKS</span></span>

[<span data-ttu-id="50899-129">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="50899-129">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)


