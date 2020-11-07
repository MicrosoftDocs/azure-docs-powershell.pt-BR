---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945975"
---
# <span data-ttu-id="a629c-101">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="a629c-101">New-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="a629c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a629c-102">SYNOPSIS</span></span>
<span data-ttu-id="a629c-103">Cria um mapeamento entre um objeto de armazenamento do Azure e um objeto de armazenamento de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a629c-103">Creates a mapping between an Azure Storage object and recovery Storage object.</span></span>

## <span data-ttu-id="a629c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a629c-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a629c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a629c-105">DESCRIPTION</span></span>
<span data-ttu-id="a629c-106">O cmdlet **New-AzureSiteRecoveryStorageMapping** cria um mapeamento entre um objeto de armazenamento primário do Azure do Azure site Recovery e um objeto de armazenamento de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a629c-106">The **New-AzureSiteRecoveryStorageMapping** cmdlet creates a mapping between an Azure Site Recovery managed primary Azure Storage object and a recovery Storage object.</span></span>

## <span data-ttu-id="a629c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a629c-107">EXAMPLES</span></span>

### <span data-ttu-id="a629c-108">Exemplo 1: criar um mapeamento entre um objeto de armazenamento e um objeto de armazenamento de recuperação</span><span class="sxs-lookup"><span data-stu-id="a629c-108">Example 1: Create a mapping between a storage object and a recovery storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

<span data-ttu-id="a629c-109">O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="a629c-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="a629c-110">O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="a629c-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="a629c-111">O segundo comando obtém o armazenamento de recuperação do site para o primeiro servidor na matriz $Servers e, em seguida, armazena-o na $Storages.</span><span class="sxs-lookup"><span data-stu-id="a629c-111">The second command gets the site recovery storage for the first server in the $Servers array, and then stores it in the $Storages.</span></span>

<span data-ttu-id="a629c-112">O comando final cria um mapeamento entre a rede principal e a rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a629c-112">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="a629c-113">O comando especifica o objeto de armazenamento principal como o primeiro elemento de $Storages.</span><span class="sxs-lookup"><span data-stu-id="a629c-113">The command specifies the primary Storage object as the first element of $Storages.</span></span>
<span data-ttu-id="a629c-114">O comando especifica o objeto de armazenamento de recuperação como o segundo elemento de $Storages.</span><span class="sxs-lookup"><span data-stu-id="a629c-114">The command specifies the recovery Storage object as the second element of $Storages.</span></span>

## <span data-ttu-id="a629c-115">OS</span><span class="sxs-lookup"><span data-stu-id="a629c-115">PARAMETERS</span></span>

### <span data-ttu-id="a629c-116">-PrimaryStorage</span><span class="sxs-lookup"><span data-stu-id="a629c-116">-PrimaryStorage</span></span>
<span data-ttu-id="a629c-117">Especifica o armazenamento primário a ser mapeado para o armazenamento de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a629c-117">Specifies the primary Storage to map to the recovery Storage.</span></span>
<span data-ttu-id="a629c-118">Para obter um objeto **ASRStorage** , use o cmdlet Get-AzureSiteRecoveryStorage.</span><span class="sxs-lookup"><span data-stu-id="a629c-118">To obtain an **ASRStorage** object, use the Get-AzureSiteRecoveryStorage cmdlet.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a629c-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a629c-119">-Profile</span></span>
<span data-ttu-id="a629c-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a629c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a629c-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a629c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a629c-122">-RecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="a629c-122">-RecoveryStorage</span></span>
<span data-ttu-id="a629c-123">Especifica o objeto de armazenamento de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a629c-123">Specifies the recovery Storage object.</span></span>
<span data-ttu-id="a629c-124">Esse cmdlet mapeia o objeto de armazenamento principal para o objeto de armazenamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a629c-124">This cmdlet maps the primary Storage object to the Storage object that this parameter specifies.</span></span>
<span data-ttu-id="a629c-125">Para obter um objeto **ASRStorage** , use **Get-AzureSiteRecoveryStorage**.</span><span class="sxs-lookup"><span data-stu-id="a629c-125">To obtain an **ASRStorage** object, use **Get-AzureSiteRecoveryStorage**.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a629c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a629c-126">CommonParameters</span></span>
<span data-ttu-id="a629c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a629c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a629c-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a629c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a629c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a629c-129">INPUTS</span></span>

## <span data-ttu-id="a629c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a629c-130">OUTPUTS</span></span>

## <span data-ttu-id="a629c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a629c-131">NOTES</span></span>

## <span data-ttu-id="a629c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a629c-132">RELATED LINKS</span></span>

[<span data-ttu-id="a629c-133">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="a629c-133">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)

[<span data-ttu-id="a629c-134">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="a629c-134">Get-AzureSiteRecoveryStorageMapping</span></span>](./Get-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="a629c-135">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="a629c-135">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


