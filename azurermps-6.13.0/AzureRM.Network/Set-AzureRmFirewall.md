---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426331"
---
# <span data-ttu-id="fbcc0-101">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fbcc0-101">Set-AzureRmFirewall</span></span>

## <span data-ttu-id="fbcc0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbcc0-102">SYNOPSIS</span></span>
<span data-ttu-id="fbcc0-103">Salva um firewall modificado.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-103">Saves a modified Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbcc0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbcc0-104">SYNTAX</span></span>

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbcc0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbcc0-105">DESCRIPTION</span></span>
<span data-ttu-id="fbcc0-106">O cmdlet **set-AzureRmFirewall** atualiza um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-106">The **Set-AzureRmFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="fbcc0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbcc0-107">EXAMPLES</span></span>

### <span data-ttu-id="fbcc0-108">1: atualizar a prioridade de um conjunto de regras de aplicativo de firewall</span><span class="sxs-lookup"><span data-stu-id="fbcc0-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

<span data-ttu-id="fbcc0-109">Este exemplo atualiza a prioridade de um conjunto de regras existente de um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="fbcc0-110">Pressupondo que o Firewall do Azure "AzureFirewall" no grupo de recursos "RG" contenha uma coleção de regras de aplicativo chamada "ruleCollectionName", os comandos acima alterarão a prioridade dessa coleção de regras e atualizarão o Firewall do Azure posteriormente.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="fbcc0-111">Sem o comando Set-AzureRmFirewall, todas as operações executadas no objeto de $azFw local não são refletidas no servidor.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-111">Without the Set-AzureRmFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="fbcc0-112">2: criar um firewall do Azure e definir uma coleção de regras de aplicativo mais tarde</span><span class="sxs-lookup"><span data-stu-id="fbcc0-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

<span data-ttu-id="fbcc0-113">Neste exemplo, um firewall é criado primeiro sem nenhuma coleção de regras de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="fbcc0-114">Posteriormente, uma regra de aplicativo e uma coleção de regras de aplicativo são criadas, o objeto de firewall é modificado na memória, sem afetar a configuração real na nuvem.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="fbcc0-115">Para que as alterações sejam refletidas na nuvem, Set-AzureRmFirewall devem ser chamadas.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-115">For changes to be reflected in cloud, Set-AzureRmFirewall must be called.</span></span>

## <span data-ttu-id="fbcc0-116">OS</span><span class="sxs-lookup"><span data-stu-id="fbcc0-116">PARAMETERS</span></span>

### <span data-ttu-id="fbcc0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbcc0-117">-AsJob</span></span>
<span data-ttu-id="fbcc0-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fbcc0-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcc0-119">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fbcc0-119">-AzureFirewall</span></span>
<span data-ttu-id="fbcc0-120">O AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fbcc0-120">The AzureFirewall</span></span>

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbcc0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbcc0-121">-DefaultProfile</span></span>
<span data-ttu-id="fbcc0-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcc0-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fbcc0-123">-Confirm</span></span>
<span data-ttu-id="fbcc0-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcc0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbcc0-125">-WhatIf</span></span>
<span data-ttu-id="fbcc0-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbcc0-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcc0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbcc0-128">CommonParameters</span></span>
<span data-ttu-id="fbcc0-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbcc0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbcc0-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbcc0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbcc0-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbcc0-131">INPUTS</span></span>

### <span data-ttu-id="fbcc0-132">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fbcc0-132">PSAzureFirewall</span></span>
<span data-ttu-id="fbcc0-133">O parâmetro ' AzureFirewall ' aceita o valor do tipo ' PSAzureFirewall ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fbcc0-133">Parameter 'AzureFirewall' accepts value of type 'PSAzureFirewall' from the pipeline</span></span>

## <span data-ttu-id="fbcc0-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbcc0-134">OUTPUTS</span></span>

### <span data-ttu-id="fbcc0-135">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fbcc0-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="fbcc0-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbcc0-136">NOTES</span></span>

## <span data-ttu-id="fbcc0-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbcc0-137">RELATED LINKS</span></span>

[<span data-ttu-id="fbcc0-138">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fbcc0-138">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="fbcc0-139">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fbcc0-139">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="fbcc0-140">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fbcc0-140">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)
