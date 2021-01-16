---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257832"
---
# <span data-ttu-id="ab64b-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="ab64b-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="ab64b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab64b-102">SYNOPSIS</span></span>
<span data-ttu-id="ab64b-103">Cria um grupo de zonas DNS privadas no ponto de extremidade privado especificado.</span><span class="sxs-lookup"><span data-stu-id="ab64b-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="ab64b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab64b-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab64b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab64b-105">DESCRIPTION</span></span>
<span data-ttu-id="ab64b-106">O cmdlet **New-AzPrivateDnsZoneGroup** permite que você crie um novo grupo de zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="ab64b-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="ab64b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab64b-107">EXAMPLES</span></span>

### <span data-ttu-id="ab64b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ab64b-108">Example 1</span></span>
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

<span data-ttu-id="ab64b-109">Após `test-pr-endpoint` a criação de um ponto de extremidade particular, acima do exemplo cria o grupo zona DNS sob esse ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ab64b-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="ab64b-110">OS</span><span class="sxs-lookup"><span data-stu-id="ab64b-110">PARAMETERS</span></span>

### <span data-ttu-id="ab64b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab64b-111">-AsJob</span></span>
<span data-ttu-id="ab64b-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ab64b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab64b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab64b-113">-DefaultProfile</span></span>
<span data-ttu-id="ab64b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab64b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab64b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ab64b-115">-Force</span></span>
<span data-ttu-id="ab64b-116">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="ab64b-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ab64b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab64b-117">-Name</span></span>
<span data-ttu-id="ab64b-118">O nome do grupo de zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="ab64b-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="ab64b-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="ab64b-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="ab64b-120">Uma coleção de configurações de zona DNS privadas do grupo de zonas DNS particulares.</span><span class="sxs-lookup"><span data-stu-id="ab64b-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="ab64b-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="ab64b-121">-PrivateEndpointName</span></span>
<span data-ttu-id="ab64b-122">O nome do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="ab64b-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="ab64b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab64b-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab64b-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ab64b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ab64b-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ab64b-125">-Confirm</span></span>
<span data-ttu-id="ab64b-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab64b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab64b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab64b-127">-WhatIf</span></span>
<span data-ttu-id="ab64b-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab64b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab64b-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab64b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab64b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab64b-130">CommonParameters</span></span>
<span data-ttu-id="ab64b-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab64b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab64b-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab64b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab64b-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab64b-133">INPUTS</span></span>

### <span data-ttu-id="ab64b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ab64b-134">System.String</span></span>

### <span data-ttu-id="ab64b-135">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. cmdlets. Network, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ab64b-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ab64b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab64b-136">OUTPUTS</span></span>

### <span data-ttu-id="ab64b-137">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="ab64b-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="ab64b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab64b-138">NOTES</span></span>

## <span data-ttu-id="ab64b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab64b-139">RELATED LINKS</span></span>
