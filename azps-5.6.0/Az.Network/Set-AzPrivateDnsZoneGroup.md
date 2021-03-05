---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 9ddd81b236303a15017bcd96da35774a16fae8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901598"
---
# <span data-ttu-id="fef57-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="fef57-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="fef57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fef57-102">SYNOPSIS</span></span>
<span data-ttu-id="fef57-103">Atualiza o grupo de zonas DNS</span><span class="sxs-lookup"><span data-stu-id="fef57-103">Updates DNS zone group</span></span>

## <span data-ttu-id="fef57-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fef57-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fef57-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fef57-105">DESCRIPTION</span></span>
<span data-ttu-id="fef57-106">O cmdlet **Set-AzPrivateDnsZoneGroup** atualiza o grupo de zonas DNS.</span><span class="sxs-lookup"><span data-stu-id="fef57-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="fef57-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fef57-107">EXAMPLES</span></span>

### <span data-ttu-id="fef57-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fef57-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]

PS C:\> $zone1 = Get-AzPrivateDnsZone -ResourceGroupName rg -Name "test1.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name test1-vault-azure-com -PrivateDnsZoneId $zone1.ResourceId
PS C:\> Set-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1 -PrivateDnsZoneConfig $config -Force

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test1-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test1.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="fef57-109">Exemplo acima atualiza o grupo de zonas DNS chamado dnsgroup1 com um novo dnsconfig que se vincula a outra zona DNS.</span><span class="sxs-lookup"><span data-stu-id="fef57-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="fef57-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fef57-110">PARAMETERS</span></span>

### <span data-ttu-id="fef57-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fef57-111">-AsJob</span></span>
<span data-ttu-id="fef57-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fef57-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fef57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef57-113">-DefaultProfile</span></span>
<span data-ttu-id="fef57-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fef57-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fef57-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fef57-115">-Name</span></span>
<span data-ttu-id="fef57-116">O nome do grupo de zona dns privado.</span><span class="sxs-lookup"><span data-stu-id="fef57-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="fef57-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="fef57-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="fef57-118">Uma coleção de configurações de zona dns privadas do grupo de zonas dns privadas.</span><span class="sxs-lookup"><span data-stu-id="fef57-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="fef57-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="fef57-119">-PrivateEndpointName</span></span>
<span data-ttu-id="fef57-120">O nome do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="fef57-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="fef57-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef57-121">-ResourceGroupName</span></span>
<span data-ttu-id="fef57-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fef57-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="fef57-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fef57-123">-Confirm</span></span>
<span data-ttu-id="fef57-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fef57-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fef57-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fef57-125">-WhatIf</span></span>
<span data-ttu-id="fef57-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fef57-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fef57-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fef57-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fef57-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef57-128">CommonParameters</span></span>
<span data-ttu-id="fef57-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fef57-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef57-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fef57-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef57-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fef57-131">INPUTS</span></span>

### <span data-ttu-id="fef57-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fef57-132">System.String</span></span>

### <span data-ttu-id="fef57-133">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="fef57-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fef57-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fef57-134">OUTPUTS</span></span>

### <span data-ttu-id="fef57-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="fef57-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="fef57-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="fef57-136">NOTES</span></span>

## <span data-ttu-id="fef57-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fef57-137">RELATED LINKS</span></span>
