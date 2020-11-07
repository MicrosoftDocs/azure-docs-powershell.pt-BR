---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 78DE0AD2-6210-4604-89A8-41915D58BD68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c40cb0fd38953ff46fa1138dc91f0b9e97ece75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945576"
---
# <span data-ttu-id="576b3-101">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="576b3-101">Get-AzureSiteRecoveryStorage</span></span>

## <span data-ttu-id="576b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="576b3-102">SYNOPSIS</span></span>
<span data-ttu-id="576b3-103">Obtém armazenamentos de recuperação de site para um cofre.</span><span class="sxs-lookup"><span data-stu-id="576b3-103">Gets Site Recovery Storages for a vault.</span></span>

## <span data-ttu-id="576b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="576b3-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorage -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="576b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="576b3-105">DESCRIPTION</span></span>
<span data-ttu-id="576b3-106">O cmdlet **Get-AzureSiteRecoveryStorage** Obtém armazenamentos do Azure site Recovery para o cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="576b3-106">The **Get-AzureSiteRecoveryStorage** cmdlet gets Azure Site Recovery Storages for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="576b3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="576b3-107">EXAMPLES</span></span>

### <span data-ttu-id="576b3-108">Exemplo 1: obter armazenamento de recuperação de site</span><span class="sxs-lookup"><span data-stu-id="576b3-108">Example 1: Get site recovery storage</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorage -Server $Servers[0]
Name           : phase2PrimaryStorageClassification
ID             : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
FabricObjectID : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM

Name           : phase2RecoveryStorageClassification
ID             : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
FabricObjectID : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM
```

<span data-ttu-id="576b3-109">O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="576b3-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="576b3-110">O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="576b3-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="576b3-111">O segundo comando obtém o armazenamento de recuperação de site para o primeiro servidor na matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="576b3-111">The second command gets the site recovery storage for the first server in the $Servers array.</span></span>

## <span data-ttu-id="576b3-112">OS</span><span class="sxs-lookup"><span data-stu-id="576b3-112">PARAMETERS</span></span>

### <span data-ttu-id="576b3-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="576b3-113">-Profile</span></span>
<span data-ttu-id="576b3-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="576b3-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="576b3-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="576b3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="576b3-116">-Servidor</span><span class="sxs-lookup"><span data-stu-id="576b3-116">-Server</span></span>
<span data-ttu-id="576b3-117">Especifica um servidor para armazenamento de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="576b3-117">Specifies a server for Azure Site Recovery Storage.</span></span>
<span data-ttu-id="576b3-118">Para obter um objeto **ASRServer** , use o cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="576b3-118">To obtain an **ASRServer** object, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="576b3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576b3-119">CommonParameters</span></span>
<span data-ttu-id="576b3-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="576b3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576b3-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="576b3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576b3-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="576b3-122">INPUTS</span></span>

## <span data-ttu-id="576b3-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="576b3-123">OUTPUTS</span></span>

## <span data-ttu-id="576b3-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="576b3-124">NOTES</span></span>

## <span data-ttu-id="576b3-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="576b3-125">RELATED LINKS</span></span>

[<span data-ttu-id="576b3-126">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="576b3-126">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


