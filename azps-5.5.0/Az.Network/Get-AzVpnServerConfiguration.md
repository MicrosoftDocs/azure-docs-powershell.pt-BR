---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112858"
---
# <span data-ttu-id="1c50d-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c50d-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="1c50d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c50d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c50d-103">Obtém uma configuração VpnServerConfiguration existente para apontar para a conectividade do site.</span><span class="sxs-lookup"><span data-stu-id="1c50d-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="1c50d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c50d-104">SYNTAX</span></span>

### <span data-ttu-id="1c50d-105">ListBySubscriptionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1c50d-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c50d-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c50d-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c50d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c50d-107">DESCRIPTION</span></span>
<span data-ttu-id="1c50d-108">O cmdlet **Get-AzVpnServerConfiguration** retorna a configuração VpnServerConfiguration existente para a conectividade ponto a site.</span><span class="sxs-lookup"><span data-stu-id="1c50d-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="1c50d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1c50d-109">EXAMPLES</span></span>

### <span data-ttu-id="1c50d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c50d-110">Example 1</span></span>
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

<span data-ttu-id="1c50d-111">O comando acima obterá o VpnServerConfiguration existente.</span><span class="sxs-lookup"><span data-stu-id="1c50d-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="1c50d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c50d-112">PARAMETERS</span></span>

### <span data-ttu-id="1c50d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c50d-113">-DefaultProfile</span></span>
<span data-ttu-id="1c50d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c50d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c50d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c50d-115">-Name</span></span>
<span data-ttu-id="1c50d-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1c50d-116">The resource name.</span></span>

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

### <span data-ttu-id="1c50d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c50d-117">-ResourceGroupName</span></span>
<span data-ttu-id="1c50d-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1c50d-118">The resource group name.</span></span>

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

### <span data-ttu-id="1c50d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c50d-119">CommonParameters</span></span>
<span data-ttu-id="1c50d-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c50d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c50d-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c50d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c50d-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="1c50d-122">INPUTS</span></span>

### <span data-ttu-id="1c50d-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1c50d-123">None</span></span>

## <span data-ttu-id="1c50d-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="1c50d-124">OUTPUTS</span></span>

### <span data-ttu-id="1c50d-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c50d-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="1c50d-126">Notas</span><span class="sxs-lookup"><span data-stu-id="1c50d-126">NOTES</span></span>

## <span data-ttu-id="1c50d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c50d-127">RELATED LINKS</span></span>
