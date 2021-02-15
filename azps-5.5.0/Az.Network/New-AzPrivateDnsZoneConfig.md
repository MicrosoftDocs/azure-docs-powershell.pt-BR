---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112819"
---
# <span data-ttu-id="7ebe4-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="7ebe4-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="7ebe4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ebe4-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebe4-103">Cria a configuração de zona DNS do grupo de zona dns particular.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="7ebe4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ebe4-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ebe4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ebe4-105">DESCRIPTION</span></span>
<span data-ttu-id="7ebe4-106">O cmdlet **New-AzPrivateDnsZoneConfig** permite que você crie um novo objeto de configuração de zona DNS que será definido no grupo de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="7ebe4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7ebe4-107">EXAMPLES</span></span>

### <span data-ttu-id="7ebe4-108">Cria configuração de zona DNS</span><span class="sxs-lookup"><span data-stu-id="7ebe4-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="7ebe4-109">O exemplo acima cria zona DNS e, em seguida, cria a configuração de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="7ebe4-110">`New-AzPrivateDnsZone` cmdlet é comprovado pelo módulo Az.PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="7ebe4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ebe4-111">PARAMETERS</span></span>

### <span data-ttu-id="7ebe4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ebe4-112">-DefaultProfile</span></span>
<span data-ttu-id="7ebe4-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ebe4-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ebe4-114">-Name</span></span>
<span data-ttu-id="7ebe4-115">Nome do recurso exclusivo dentro de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="7ebe4-116">Esse nome pode ser usado para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="7ebe4-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="7ebe4-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="7ebe4-118">A ID do recurso da zona dns privada.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="7ebe4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebe4-119">CommonParameters</span></span>
<span data-ttu-id="7ebe4-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebe4-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ebe4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebe4-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="7ebe4-122">INPUTS</span></span>

### <span data-ttu-id="7ebe4-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7ebe4-123">None</span></span>

## <span data-ttu-id="7ebe4-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="7ebe4-124">OUTPUTS</span></span>

### <span data-ttu-id="7ebe4-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="7ebe4-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="7ebe4-126">Notas</span><span class="sxs-lookup"><span data-stu-id="7ebe4-126">NOTES</span></span>

## <span data-ttu-id="7ebe4-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ebe4-127">RELATED LINKS</span></span>
