---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 955c5200b7c7b9716e096f1157f7179619ae4f5c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785310"
---
# <span data-ttu-id="c181d-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c181d-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="c181d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c181d-102">SYNOPSIS</span></span>
<span data-ttu-id="c181d-103">Remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="c181d-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c181d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c181d-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c181d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c181d-105">DESCRIPTION</span></span>
<span data-ttu-id="c181d-106">O cmdlet **Remove-AzureRmNetworkInterface** remove uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="c181d-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="c181d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c181d-107">EXAMPLES</span></span>

### <span data-ttu-id="c181d-108">Exemplo 1: remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="c181d-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="c181d-109">Esse comando Remove a interface de NetworkInterface1 na ResourceGroup1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c181d-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="c181d-110">Como o parâmetro *Force* não é usado, o usuário será solicitado a confirmar essa ação.</span><span class="sxs-lookup"><span data-stu-id="c181d-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="c181d-111">Exemplo 2: remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="c181d-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="c181d-112">Esse comando Remove todas as interfaces de rede na ResourceGroup1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c181d-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="c181d-113">Como o parâmetro *Force* é usado, o usuário não será solicitado a confirmar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="c181d-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="c181d-114">OS</span><span class="sxs-lookup"><span data-stu-id="c181d-114">PARAMETERS</span></span>

### <span data-ttu-id="c181d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c181d-115">-AsJob</span></span>
<span data-ttu-id="c181d-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c181d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c181d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c181d-117">-DefaultProfile</span></span>
<span data-ttu-id="c181d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c181d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c181d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c181d-119">-Force</span></span>
<span data-ttu-id="c181d-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c181d-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c181d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c181d-121">-Name</span></span>
<span data-ttu-id="c181d-122">Especifica o nome da interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c181d-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c181d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c181d-123">-PassThru</span></span>
<span data-ttu-id="c181d-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c181d-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c181d-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c181d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c181d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c181d-126">-ResourceGroupName</span></span>
<span data-ttu-id="c181d-127">Especifica o nome de um grupo de recursos que contém a interface de rede que esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c181d-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c181d-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c181d-128">-Confirm</span></span>
<span data-ttu-id="c181d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c181d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c181d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c181d-130">-WhatIf</span></span>
<span data-ttu-id="c181d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c181d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c181d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c181d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c181d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c181d-133">CommonParameters</span></span>
<span data-ttu-id="c181d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c181d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c181d-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c181d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c181d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c181d-136">INPUTS</span></span>

## <span data-ttu-id="c181d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c181d-137">OUTPUTS</span></span>

## <span data-ttu-id="c181d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c181d-138">NOTES</span></span>

## <span data-ttu-id="c181d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c181d-139">RELATED LINKS</span></span>

[<span data-ttu-id="c181d-140">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c181d-140">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="c181d-141">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c181d-141">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="c181d-142">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c181d-142">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


