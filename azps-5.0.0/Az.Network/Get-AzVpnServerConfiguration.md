---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118123"
---
# <span data-ttu-id="bb5cc-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb5cc-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="bb5cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb5cc-103">Obtém um VpnServerConfiguration existente para a conectividade do ponto para o site.</span><span class="sxs-lookup"><span data-stu-id="bb5cc-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="bb5cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb5cc-104">SYNTAX</span></span>

### <span data-ttu-id="bb5cc-105">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb5cc-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb5cc-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb5cc-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb5cc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb5cc-107">DESCRIPTION</span></span>
<span data-ttu-id="bb5cc-108">O cmdlet **Get-AzVpnServerConfiguration** retorna o VpnServerConfiguration existente do ponto para a conectividade do site.</span><span class="sxs-lookup"><span data-stu-id="bb5cc-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="bb5cc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb5cc-109">EXAMPLES</span></span>

### <span data-ttu-id="bb5cc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb5cc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name test1config

ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="bb5cc-111">O comando acima receberá o VpnServerConfiguration existente.</span><span class="sxs-lookup"><span data-stu-id="bb5cc-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="bb5cc-112">OS</span><span class="sxs-lookup"><span data-stu-id="bb5cc-112">PARAMETERS</span></span>

### <span data-ttu-id="bb5cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb5cc-113">-DefaultProfile</span></span>
<span data-ttu-id="bb5cc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5cc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb5cc-115">-Name</span></span>
<span data-ttu-id="bb5cc-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="bb5cc-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnServerConfigurationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb5cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb5cc-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb5cc-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb5cc-119">CommonParameters</span></span>
<span data-ttu-id="bb5cc-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb5cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb5cc-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb5cc-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb5cc-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb5cc-122">INPUTS</span></span>

### <span data-ttu-id="bb5cc-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bb5cc-123">None</span></span>

## <span data-ttu-id="bb5cc-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb5cc-124">OUTPUTS</span></span>

### <span data-ttu-id="bb5cc-125">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb5cc-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="bb5cc-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb5cc-126">NOTES</span></span>

## <span data-ttu-id="bb5cc-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb5cc-127">RELATED LINKS</span></span>
