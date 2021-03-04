---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: 8ef418202025e7525dd5da74219501f11e69a5a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886175"
---
# <span data-ttu-id="74c18-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="74c18-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="74c18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74c18-102">SYNOPSIS</span></span>
<span data-ttu-id="74c18-103">Cria a configuração de zona DNS do grupo de zonas dns privada.</span><span class="sxs-lookup"><span data-stu-id="74c18-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="74c18-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="74c18-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74c18-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="74c18-105">DESCRIPTION</span></span>
<span data-ttu-id="74c18-106">O cmdlet **New-AzPrivateDnsZoneConfig** permite que você crie um novo objeto de configuração de zona DNS que será definido no grupo de zonas DNS.</span><span class="sxs-lookup"><span data-stu-id="74c18-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="74c18-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74c18-107">EXAMPLES</span></span>

### <span data-ttu-id="74c18-108">Cria configuração de zona DNS</span><span class="sxs-lookup"><span data-stu-id="74c18-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="74c18-109">O exemplo acima cria zona DNS e, em seguida, cria a configuração de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="74c18-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="74c18-110">`New-AzPrivateDnsZone` cmdlet é comprovado pelo módulo Az.PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="74c18-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="74c18-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="74c18-111">PARAMETERS</span></span>

### <span data-ttu-id="74c18-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c18-112">-DefaultProfile</span></span>
<span data-ttu-id="74c18-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74c18-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74c18-114">-Name</span><span class="sxs-lookup"><span data-stu-id="74c18-114">-Name</span></span>
<span data-ttu-id="74c18-115">Nome do recurso exclusivo em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74c18-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="74c18-116">Esse nome pode ser usado para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="74c18-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="74c18-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="74c18-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="74c18-118">A id de recurso da zona dns privada.</span><span class="sxs-lookup"><span data-stu-id="74c18-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="74c18-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c18-119">CommonParameters</span></span>
<span data-ttu-id="74c18-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c18-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c18-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74c18-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c18-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74c18-122">INPUTS</span></span>

### <span data-ttu-id="74c18-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="74c18-123">None</span></span>

## <span data-ttu-id="74c18-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="74c18-124">OUTPUTS</span></span>

### <span data-ttu-id="74c18-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="74c18-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="74c18-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="74c18-126">NOTES</span></span>

## <span data-ttu-id="74c18-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74c18-127">RELATED LINKS</span></span>
