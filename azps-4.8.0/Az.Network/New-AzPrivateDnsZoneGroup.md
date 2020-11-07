---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955403"
---
# <span data-ttu-id="9dc35-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="9dc35-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="9dc35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9dc35-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc35-103">Cria um grupo de zonas DNS privadas no ponto de extremidade privado especificado.</span><span class="sxs-lookup"><span data-stu-id="9dc35-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="9dc35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dc35-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dc35-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9dc35-105">DESCRIPTION</span></span>
<span data-ttu-id="9dc35-106">O cmdlet **New-AzPrivateDnsZoneGroup** permite que você crie um novo grupo de zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="9dc35-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="9dc35-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9dc35-107">EXAMPLES</span></span>

### <span data-ttu-id="9dc35-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9dc35-108">Example 1</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
PS C:\> New-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1" -PrivateDnsZoneConfig $config -Force
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

<span data-ttu-id="9dc35-109">Após `test-pr-endpoint` a criação de um ponto de extremidade particular, acima do exemplo cria o grupo zona DNS sob esse ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="9dc35-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="9dc35-110">OS</span><span class="sxs-lookup"><span data-stu-id="9dc35-110">PARAMETERS</span></span>

### <span data-ttu-id="9dc35-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dc35-111">-AsJob</span></span>
<span data-ttu-id="9dc35-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9dc35-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc35-113">-DefaultProfile</span></span>
<span data-ttu-id="9dc35-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9dc35-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dc35-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9dc35-115">-Force</span></span>
<span data-ttu-id="9dc35-116">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="9dc35-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc35-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9dc35-117">-Name</span></span>
<span data-ttu-id="9dc35-118">O nome do grupo de zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="9dc35-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc35-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="9dc35-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="9dc35-120">Uma coleção de configurações de zona DNS privadas do grupo de zonas DNS particulares.</span><span class="sxs-lookup"><span data-stu-id="9dc35-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc35-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="9dc35-121">-PrivateEndpointName</span></span>
<span data-ttu-id="9dc35-122">O nome do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="9dc35-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="9dc35-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dc35-123">-ResourceGroupName</span></span>
<span data-ttu-id="9dc35-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9dc35-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9dc35-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9dc35-125">-Confirm</span></span>
<span data-ttu-id="9dc35-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dc35-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc35-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc35-127">-WhatIf</span></span>
<span data-ttu-id="9dc35-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9dc35-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc35-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9dc35-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc35-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc35-130">CommonParameters</span></span>
<span data-ttu-id="9dc35-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dc35-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc35-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dc35-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc35-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9dc35-133">INPUTS</span></span>

### <span data-ttu-id="9dc35-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9dc35-134">System.String</span></span>

### <span data-ttu-id="9dc35-135">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. cmdlets. Network, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9dc35-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9dc35-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9dc35-136">OUTPUTS</span></span>

### <span data-ttu-id="9dc35-137">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="9dc35-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="9dc35-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9dc35-138">NOTES</span></span>

## <span data-ttu-id="9dc35-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9dc35-139">RELATED LINKS</span></span>
