---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112818"
---
# <span data-ttu-id="a4baf-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="a4baf-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a4baf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4baf-102">SYNOPSIS</span></span>
<span data-ttu-id="a4baf-103">Cria um grupo de zona DNS particular no ponto de extremidade particular especificado.</span><span class="sxs-lookup"><span data-stu-id="a4baf-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="a4baf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4baf-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4baf-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4baf-105">DESCRIPTION</span></span>
<span data-ttu-id="a4baf-106">O cmdlet **New-AzPrivateDnsZoneGroup** permite que você crie um novo grupo de zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="a4baf-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="a4baf-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4baf-107">EXAMPLES</span></span>

### <span data-ttu-id="a4baf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4baf-108">Example 1</span></span>
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

<span data-ttu-id="a4baf-109">Depois que o ponto de extremidade particular é criado, o exemplo acima cria um `test-pr-endpoint` grupo de zona DNS sob esse ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="a4baf-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="a4baf-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4baf-110">PARAMETERS</span></span>

### <span data-ttu-id="a4baf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4baf-111">-AsJob</span></span>
<span data-ttu-id="a4baf-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a4baf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4baf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4baf-113">-DefaultProfile</span></span>
<span data-ttu-id="a4baf-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4baf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4baf-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a4baf-115">-Force</span></span>
<span data-ttu-id="a4baf-116">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="a4baf-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a4baf-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4baf-117">-Name</span></span>
<span data-ttu-id="a4baf-118">O nome do grupo de zona dns particular.</span><span class="sxs-lookup"><span data-stu-id="a4baf-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="a4baf-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="a4baf-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="a4baf-120">Um conjunto de configurações privadas de zona dns do grupo de zona dns particular.</span><span class="sxs-lookup"><span data-stu-id="a4baf-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="a4baf-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="a4baf-121">-PrivateEndpointName</span></span>
<span data-ttu-id="a4baf-122">O nome do ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="a4baf-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="a4baf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4baf-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4baf-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4baf-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4baf-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a4baf-125">-Confirm</span></span>
<span data-ttu-id="a4baf-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4baf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4baf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4baf-127">-WhatIf</span></span>
<span data-ttu-id="a4baf-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a4baf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4baf-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4baf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4baf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4baf-130">CommonParameters</span></span>
<span data-ttu-id="a4baf-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4baf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4baf-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4baf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4baf-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="a4baf-133">INPUTS</span></span>

### <span data-ttu-id="a4baf-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a4baf-134">System.String</span></span>

### <span data-ttu-id="a4baf-135">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a4baf-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a4baf-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="a4baf-136">OUTPUTS</span></span>

### <span data-ttu-id="a4baf-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="a4baf-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a4baf-138">Notas</span><span class="sxs-lookup"><span data-stu-id="a4baf-138">NOTES</span></span>

## <span data-ttu-id="a4baf-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4baf-139">RELATED LINKS</span></span>
