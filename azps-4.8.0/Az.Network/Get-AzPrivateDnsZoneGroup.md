---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111060"
---
# <span data-ttu-id="32cbe-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="32cbe-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="32cbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="32cbe-103">É um grupo de zona DNS privada</span><span class="sxs-lookup"><span data-stu-id="32cbe-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="32cbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32cbe-104">SYNTAX</span></span>

### <span data-ttu-id="32cbe-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="32cbe-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32cbe-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="32cbe-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32cbe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32cbe-107">DESCRIPTION</span></span>
<span data-ttu-id="32cbe-108">O cmdlet **Get-AzPrivateDnsZoneGroup** Obtém um ou mais grupos de zona DNS particulares.</span><span class="sxs-lookup"><span data-stu-id="32cbe-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="32cbe-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32cbe-109">EXAMPLES</span></span>

### <span data-ttu-id="32cbe-110">Exemplo 1: recuperar o grupo de zona DNS privada</span><span class="sxs-lookup"><span data-stu-id="32cbe-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="32cbe-111">O exemplo acima Obtém um grupo de zona DNS particular chamado dnsgroup1 no RG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32cbe-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="32cbe-112">OS</span><span class="sxs-lookup"><span data-stu-id="32cbe-112">PARAMETERS</span></span>

### <span data-ttu-id="32cbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32cbe-113">-DefaultProfile</span></span>
<span data-ttu-id="32cbe-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32cbe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32cbe-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="32cbe-115">-Name</span></span>
<span data-ttu-id="32cbe-116">O nome do grupo de zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="32cbe-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cbe-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="32cbe-117">-PrivateEndpointName</span></span>
<span data-ttu-id="32cbe-118">O nome do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="32cbe-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cbe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32cbe-119">-ResourceGroupName</span></span>
<span data-ttu-id="32cbe-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32cbe-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cbe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cbe-121">CommonParameters</span></span>
<span data-ttu-id="32cbe-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32cbe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cbe-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32cbe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cbe-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32cbe-124">INPUTS</span></span>

### <span data-ttu-id="32cbe-125">System. String</span><span class="sxs-lookup"><span data-stu-id="32cbe-125">System.String</span></span>

## <span data-ttu-id="32cbe-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32cbe-126">OUTPUTS</span></span>

### <span data-ttu-id="32cbe-127">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="32cbe-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="32cbe-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32cbe-128">NOTES</span></span>

## <span data-ttu-id="32cbe-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32cbe-129">RELATED LINKS</span></span>
