---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
ms.openlocfilehash: ebf2a58530f1dabe0e320dd78a38c63c86565c73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610278"
---
# <span data-ttu-id="9b003-101">Remove-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9b003-101">Remove-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="9b003-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b003-102">SYNOPSIS</span></span>
<span data-ttu-id="9b003-103">Remove um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9b003-103">Removes a network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b003-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b003-104">SYNTAX</span></span>

### <span data-ttu-id="9b003-105">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="9b003-105">RemoveByName</span></span>
```
Remove-AzureRmNetworkProfile -ResourceGroupName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b003-106">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b003-106">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b003-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b003-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b003-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b003-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b003-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b003-109">DESCRIPTION</span></span>
<span data-ttu-id="9b003-110">O cmdlet **Remove-AzureRmNetworkProfile** remove um perfil de rede se não for criada nenhuma interface de rede de contêiner (conforme o contraste com uma **configuração** de interface de rede de contêiner).</span><span class="sxs-lookup"><span data-stu-id="9b003-110">The **Remove-AzureRmNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="9b003-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b003-111">EXAMPLES</span></span>

### <span data-ttu-id="9b003-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b003-112">Example 1</span></span>
```powershell
Remove-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="9b003-113">Isso remove o perfil de rede com o nome NP1 da Rg1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b003-113">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="9b003-114">OS</span><span class="sxs-lookup"><span data-stu-id="9b003-114">PARAMETERS</span></span>

### <span data-ttu-id="9b003-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b003-115">-AsJob</span></span>
<span data-ttu-id="9b003-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9b003-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b003-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b003-117">-DefaultProfile</span></span>
<span data-ttu-id="9b003-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b003-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b003-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9b003-119">-Force</span></span>
<span data-ttu-id="9b003-120">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="9b003-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="9b003-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b003-121">-InputObject</span></span>
<span data-ttu-id="9b003-122">Objeto de perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9b003-122">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b003-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b003-123">-Name</span></span>
<span data-ttu-id="9b003-124">O nome do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9b003-124">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b003-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b003-125">-PassThru</span></span>
<span data-ttu-id="9b003-126">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="9b003-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9b003-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b003-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b003-128">O nome do grupo de recursos do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9b003-128">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b003-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b003-129">-ResourceId</span></span>
<span data-ttu-id="9b003-130">A ID do recurso do Gerenciador de recursos do Azure do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9b003-130">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b003-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b003-131">-Confirm</span></span>
<span data-ttu-id="9b003-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b003-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b003-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b003-133">-WhatIf</span></span>
<span data-ttu-id="9b003-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b003-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b003-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b003-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b003-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b003-136">CommonParameters</span></span>
<span data-ttu-id="9b003-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b003-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b003-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b003-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b003-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b003-139">INPUTS</span></span>

### <span data-ttu-id="9b003-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9b003-140">System.String</span></span>

## <span data-ttu-id="9b003-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b003-141">OUTPUTS</span></span>

### <span data-ttu-id="9b003-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b003-142">System.Boolean</span></span>

## <span data-ttu-id="9b003-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b003-143">NOTES</span></span>

## <span data-ttu-id="9b003-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b003-144">RELATED LINKS</span></span>
