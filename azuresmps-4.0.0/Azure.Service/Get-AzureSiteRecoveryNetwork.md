---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96b51b49d76093be96eeab26417f4a70f70c4627
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945592"
---
# <span data-ttu-id="a853c-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="a853c-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="a853c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a853c-102">SYNOPSIS</span></span>
<span data-ttu-id="a853c-103">Obtém informações sobre as redes gerenciadas pela recuperação de site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="a853c-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="a853c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a853c-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a853c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a853c-105">DESCRIPTION</span></span>
<span data-ttu-id="a853c-106">O cmdlet **Get-AzureSiteRecoveryNetwork** Obtém informações sobre as redes de recuperação de site do Azure para o cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="a853c-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="a853c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a853c-107">EXAMPLES</span></span>

### <span data-ttu-id="a853c-108">Exemplo 1: obter redes de recuperação de sites</span><span class="sxs-lookup"><span data-stu-id="a853c-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="a853c-109">O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="a853c-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="a853c-110">O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="a853c-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="a853c-111">O segundo comando obtém a rede de recuperação de site para o primeiro servidor na matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="a853c-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="a853c-112">OS</span><span class="sxs-lookup"><span data-stu-id="a853c-112">PARAMETERS</span></span>

### <span data-ttu-id="a853c-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a853c-113">-Profile</span></span>
<span data-ttu-id="a853c-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a853c-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a853c-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a853c-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a853c-116">-Servidor</span><span class="sxs-lookup"><span data-stu-id="a853c-116">-Server</span></span>
<span data-ttu-id="a853c-117">Especifica um servidor de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="a853c-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="a853c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a853c-118">CommonParameters</span></span>
<span data-ttu-id="a853c-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a853c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a853c-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a853c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a853c-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a853c-121">INPUTS</span></span>

## <span data-ttu-id="a853c-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a853c-122">OUTPUTS</span></span>

## <span data-ttu-id="a853c-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a853c-123">NOTES</span></span>

## <span data-ttu-id="a853c-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a853c-124">RELATED LINKS</span></span>

[<span data-ttu-id="a853c-125">Cmdlets de serviços de recuperação do site do Azure</span><span class="sxs-lookup"><span data-stu-id="a853c-125">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


