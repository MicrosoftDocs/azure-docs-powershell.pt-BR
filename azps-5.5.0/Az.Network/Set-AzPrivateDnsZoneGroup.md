---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112762"
---
# <span data-ttu-id="a76c2-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="a76c2-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a76c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a76c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a76c2-103">Atualiza o grupo de zona DNS</span><span class="sxs-lookup"><span data-stu-id="a76c2-103">Updates DNS zone group</span></span>

## <span data-ttu-id="a76c2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a76c2-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a76c2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a76c2-105">DESCRIPTION</span></span>
<span data-ttu-id="a76c2-106">O cmdlet **Set-AzPrivateDnsZoneGroup** atualiza o grupo de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="a76c2-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="a76c2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a76c2-107">EXAMPLES</span></span>

### <span data-ttu-id="a76c2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a76c2-108">Example 1</span></span>
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

<span data-ttu-id="a76c2-109">Acima do exemplo, atualiza o grupo de zona DNS chamado dnsgroup1 com uma nova dnsconfig que vincula a outra zona DNS.</span><span class="sxs-lookup"><span data-stu-id="a76c2-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="a76c2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a76c2-110">PARAMETERS</span></span>

### <span data-ttu-id="a76c2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a76c2-111">-AsJob</span></span>
<span data-ttu-id="a76c2-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a76c2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a76c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76c2-113">-DefaultProfile</span></span>
<span data-ttu-id="a76c2-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a76c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a76c2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a76c2-115">-Name</span></span>
<span data-ttu-id="a76c2-116">O nome do grupo de zona dns particular.</span><span class="sxs-lookup"><span data-stu-id="a76c2-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="a76c2-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="a76c2-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="a76c2-118">Um conjunto de configurações privadas de zona dns do grupo de zona dns particular.</span><span class="sxs-lookup"><span data-stu-id="a76c2-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="a76c2-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="a76c2-119">-PrivateEndpointName</span></span>
<span data-ttu-id="a76c2-120">O nome do ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="a76c2-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="a76c2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a76c2-121">-ResourceGroupName</span></span>
<span data-ttu-id="a76c2-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a76c2-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a76c2-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a76c2-123">-Confirm</span></span>
<span data-ttu-id="a76c2-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a76c2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a76c2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76c2-125">-WhatIf</span></span>
<span data-ttu-id="a76c2-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a76c2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a76c2-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a76c2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a76c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76c2-128">CommonParameters</span></span>
<span data-ttu-id="a76c2-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a76c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76c2-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a76c2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76c2-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="a76c2-131">INPUTS</span></span>

### <span data-ttu-id="a76c2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a76c2-132">System.String</span></span>

### <span data-ttu-id="a76c2-133">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a76c2-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a76c2-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="a76c2-134">OUTPUTS</span></span>

### <span data-ttu-id="a76c2-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="a76c2-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a76c2-136">Notas</span><span class="sxs-lookup"><span data-stu-id="a76c2-136">NOTES</span></span>

## <span data-ttu-id="a76c2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a76c2-137">RELATED LINKS</span></span>
