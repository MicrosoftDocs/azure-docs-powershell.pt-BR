---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114649"
---
# <span data-ttu-id="10691-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="10691-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="10691-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10691-102">SYNOPSIS</span></span>
<span data-ttu-id="10691-103">Remove um grupo de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="10691-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="10691-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10691-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10691-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="10691-105">DESCRIPTION</span></span>
<span data-ttu-id="10691-106">O cmdlet **Remove-AzPrivateDnsZoneGroup** remove um grupo de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="10691-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="10691-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10691-107">EXAMPLES</span></span>

### <span data-ttu-id="10691-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10691-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="10691-109">Exemplo acima remove uma zona DNS chamada dnsgroup1 do ponto de extremidade test-pr-endpoint.</span><span class="sxs-lookup"><span data-stu-id="10691-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="10691-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10691-110">PARAMETERS</span></span>

### <span data-ttu-id="10691-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10691-111">-AsJob</span></span>
<span data-ttu-id="10691-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="10691-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10691-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10691-113">-DefaultProfile</span></span>
<span data-ttu-id="10691-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10691-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10691-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="10691-115">-Force</span></span>
<span data-ttu-id="10691-116">Não peça confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="10691-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="10691-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="10691-117">-Name</span></span>
<span data-ttu-id="10691-118">O nome do grupo de zona dns particular.</span><span class="sxs-lookup"><span data-stu-id="10691-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="10691-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10691-119">-PassThru</span></span>
<span data-ttu-id="10691-120">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="10691-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="10691-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="10691-121">-PrivateEndpointName</span></span>
<span data-ttu-id="10691-122">O nome do ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="10691-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="10691-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10691-123">-ResourceGroupName</span></span>
<span data-ttu-id="10691-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10691-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="10691-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="10691-125">-Confirm</span></span>
<span data-ttu-id="10691-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10691-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10691-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10691-127">-WhatIf</span></span>
<span data-ttu-id="10691-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="10691-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10691-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10691-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10691-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10691-130">CommonParameters</span></span>
<span data-ttu-id="10691-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10691-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10691-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10691-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10691-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="10691-133">INPUTS</span></span>

### <span data-ttu-id="10691-134">System.String</span><span class="sxs-lookup"><span data-stu-id="10691-134">System.String</span></span>

## <span data-ttu-id="10691-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="10691-135">OUTPUTS</span></span>

### <span data-ttu-id="10691-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10691-136">System.Boolean</span></span>

## <span data-ttu-id="10691-137">Notas</span><span class="sxs-lookup"><span data-stu-id="10691-137">NOTES</span></span>

## <span data-ttu-id="10691-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10691-138">RELATED LINKS</span></span>
