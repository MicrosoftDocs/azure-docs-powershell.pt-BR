---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257412"
---
# <span data-ttu-id="da581-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="da581-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="da581-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da581-102">SYNOPSIS</span></span>
<span data-ttu-id="da581-103">Remove um grupo de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="da581-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="da581-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da581-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da581-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da581-105">DESCRIPTION</span></span>
<span data-ttu-id="da581-106">O cmdlet **Remove-AzPrivateDnsZoneGroup** remove um grupo de zonas DNS.</span><span class="sxs-lookup"><span data-stu-id="da581-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="da581-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da581-107">EXAMPLES</span></span>

### <span data-ttu-id="da581-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da581-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="da581-109">Exemplo acima remove um Grup de zona DNS chamado dnsgroup1 do Endpoint Test-PR-Endpoint.</span><span class="sxs-lookup"><span data-stu-id="da581-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="da581-110">OS</span><span class="sxs-lookup"><span data-stu-id="da581-110">PARAMETERS</span></span>

### <span data-ttu-id="da581-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da581-111">-AsJob</span></span>
<span data-ttu-id="da581-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="da581-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da581-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da581-113">-DefaultProfile</span></span>
<span data-ttu-id="da581-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da581-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da581-115">-Force</span><span class="sxs-lookup"><span data-stu-id="da581-115">-Force</span></span>
<span data-ttu-id="da581-116">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="da581-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="da581-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="da581-117">-Name</span></span>
<span data-ttu-id="da581-118">O nome do grupo de zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="da581-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="da581-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da581-119">-PassThru</span></span>
<span data-ttu-id="da581-120">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="da581-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="da581-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="da581-121">-PrivateEndpointName</span></span>
<span data-ttu-id="da581-122">O nome do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="da581-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="da581-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da581-123">-ResourceGroupName</span></span>
<span data-ttu-id="da581-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="da581-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="da581-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da581-125">-Confirm</span></span>
<span data-ttu-id="da581-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da581-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da581-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da581-127">-WhatIf</span></span>
<span data-ttu-id="da581-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da581-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da581-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da581-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da581-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da581-130">CommonParameters</span></span>
<span data-ttu-id="da581-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da581-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da581-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da581-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da581-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da581-133">INPUTS</span></span>

### <span data-ttu-id="da581-134">System. String</span><span class="sxs-lookup"><span data-stu-id="da581-134">System.String</span></span>

## <span data-ttu-id="da581-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da581-135">OUTPUTS</span></span>

### <span data-ttu-id="da581-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da581-136">System.Boolean</span></span>

## <span data-ttu-id="da581-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da581-137">NOTES</span></span>

## <span data-ttu-id="da581-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da581-138">RELATED LINKS</span></span>
