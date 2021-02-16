---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a5701fc6308f1884bbf0237887a223a62a58669
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411578"
---
# <span data-ttu-id="78464-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="78464-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="78464-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78464-102">SYNOPSIS</span></span>
<span data-ttu-id="78464-103">Obtém informações sobre as redes gerenciadas pela Recuperação de Site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="78464-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="78464-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78464-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="78464-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="78464-105">DESCRIPTION</span></span>
<span data-ttu-id="78464-106">O cmdlet **Get-AzureSiteRecoveryNetwork** obtém informações sobre redes de Recuperação de Site do Azure para o cofre atual de Recuperação de Sites.</span><span class="sxs-lookup"><span data-stu-id="78464-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="78464-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78464-107">EXAMPLES</span></span>

### <span data-ttu-id="78464-108">Exemplo 1: Obter redes de recuperação de sites</span><span class="sxs-lookup"><span data-stu-id="78464-108">Example 1: Get site recovery networks</span></span>
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

<span data-ttu-id="78464-109">O primeiro cmdlet de comando obtém servidores para o cofre atual de Recuperação de Site do Azure usando o cmdlet **Get-AzureSiteRecoveryServer.**</span><span class="sxs-lookup"><span data-stu-id="78464-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="78464-110">O comando armazena os servidores de Recuperação de Site na variável $Servers matriz.</span><span class="sxs-lookup"><span data-stu-id="78464-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="78464-111">O segundo comando obtém a rede de recuperação do site para o primeiro servidor na matriz $Servers dados.</span><span class="sxs-lookup"><span data-stu-id="78464-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="78464-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78464-112">PARAMETERS</span></span>

### <span data-ttu-id="78464-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="78464-113">-Profile</span></span>
<span data-ttu-id="78464-114">Especifica o perfil do Azure a partir do qual este cmdlet é lido.</span><span class="sxs-lookup"><span data-stu-id="78464-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="78464-115">Se você não especificar um perfil, esse cmdlet será lido do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="78464-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78464-116">-Server</span><span class="sxs-lookup"><span data-stu-id="78464-116">-Server</span></span>
<span data-ttu-id="78464-117">Especifica um servidor de Recuperação de Site.</span><span class="sxs-lookup"><span data-stu-id="78464-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="78464-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78464-118">CommonParameters</span></span>
<span data-ttu-id="78464-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78464-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78464-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78464-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78464-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="78464-121">INPUTS</span></span>

## <span data-ttu-id="78464-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="78464-122">OUTPUTS</span></span>

## <span data-ttu-id="78464-123">Notas</span><span class="sxs-lookup"><span data-stu-id="78464-123">NOTES</span></span>

## <span data-ttu-id="78464-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78464-124">RELATED LINKS</span></span>




