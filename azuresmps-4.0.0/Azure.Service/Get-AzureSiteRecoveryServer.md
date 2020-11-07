---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4081d6d072aadd6a4ae7d09ff57748a8f2cb697
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945580"
---
# <span data-ttu-id="bd874-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="bd874-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="bd874-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd874-102">SYNOPSIS</span></span>
<span data-ttu-id="bd874-103">Obtém os servidores de recuperação de site registrados um cofre de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="bd874-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="bd874-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd874-104">SYNTAX</span></span>

### <span data-ttu-id="bd874-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="bd874-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bd874-106">ById</span><span class="sxs-lookup"><span data-stu-id="bd874-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bd874-107">ByName</span><span class="sxs-lookup"><span data-stu-id="bd874-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bd874-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd874-108">DESCRIPTION</span></span>
<span data-ttu-id="bd874-109">O cmdlet **Get-AzureSiteRecoveryServer** Obtém informações sobre os servidores de recuperação de site do Azure registrados no cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="bd874-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="bd874-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd874-110">EXAMPLES</span></span>

### <span data-ttu-id="bd874-111">Exemplo 1: obter informações sobre um servidor de recuperação de site</span><span class="sxs-lookup"><span data-stu-id="bd874-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="bd874-112">Esse comando obtém informações sobre um servidor do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="bd874-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="bd874-113">OS</span><span class="sxs-lookup"><span data-stu-id="bd874-113">PARAMETERS</span></span>

### <span data-ttu-id="bd874-114">-ID</span><span class="sxs-lookup"><span data-stu-id="bd874-114">-Id</span></span>
<span data-ttu-id="bd874-115">Especifica a ID de um servidor.</span><span class="sxs-lookup"><span data-stu-id="bd874-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd874-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd874-116">-Name</span></span>
<span data-ttu-id="bd874-117">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="bd874-117">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd874-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bd874-118">-Profile</span></span>
<span data-ttu-id="bd874-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bd874-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bd874-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bd874-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bd874-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd874-121">CommonParameters</span></span>
<span data-ttu-id="bd874-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd874-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd874-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd874-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd874-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd874-124">INPUTS</span></span>

## <span data-ttu-id="bd874-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd874-125">OUTPUTS</span></span>

## <span data-ttu-id="bd874-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd874-126">NOTES</span></span>

## <span data-ttu-id="bd874-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd874-127">RELATED LINKS</span></span>

[<span data-ttu-id="bd874-128">Cmdlets de serviços de recuperação do site do Azure</span><span class="sxs-lookup"><span data-stu-id="bd874-128">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


