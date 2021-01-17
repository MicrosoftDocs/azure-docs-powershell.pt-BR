---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427562"
---
# <span data-ttu-id="937ad-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="937ad-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="937ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="937ad-102">SYNOPSIS</span></span>
<span data-ttu-id="937ad-103">Cria a configuração de zona DNS do grupo de zonas DNS particulares.</span><span class="sxs-lookup"><span data-stu-id="937ad-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="937ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="937ad-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="937ad-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="937ad-105">DESCRIPTION</span></span>
<span data-ttu-id="937ad-106">O cmdlet **New-AzPrivateDnsZoneConfig** permite que você crie um novo objeto de configuração de zona DNS que será definido no grupo zona DNS.</span><span class="sxs-lookup"><span data-stu-id="937ad-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="937ad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="937ad-107">EXAMPLES</span></span>

### <span data-ttu-id="937ad-108">Cria a configuração de zona DNS</span><span class="sxs-lookup"><span data-stu-id="937ad-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="937ad-109">O exemplo acima cria uma zona DNS e, em seguida, cria a configuração de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="937ad-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="937ad-110">`New-AzPrivateDnsZone` o cmdlet é comprovado pelo módulo AZ. PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="937ad-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="937ad-111">OS</span><span class="sxs-lookup"><span data-stu-id="937ad-111">PARAMETERS</span></span>

### <span data-ttu-id="937ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937ad-112">-DefaultProfile</span></span>
<span data-ttu-id="937ad-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="937ad-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="937ad-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="937ad-114">-Name</span></span>
<span data-ttu-id="937ad-115">Nome do recurso exclusivo dentro de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="937ad-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="937ad-116">Esse nome pode ser usado para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="937ad-116">This name can be used to access the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="937ad-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="937ad-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="937ad-118">A ID do recurso da zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="937ad-118">The resource id of the private dns zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="937ad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937ad-119">CommonParameters</span></span>
<span data-ttu-id="937ad-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="937ad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937ad-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="937ad-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937ad-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="937ad-122">INPUTS</span></span>

### <span data-ttu-id="937ad-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="937ad-123">None</span></span>

## <span data-ttu-id="937ad-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="937ad-124">OUTPUTS</span></span>

### <span data-ttu-id="937ad-125">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="937ad-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="937ad-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="937ad-126">NOTES</span></span>

## <span data-ttu-id="937ad-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="937ad-127">RELATED LINKS</span></span>
