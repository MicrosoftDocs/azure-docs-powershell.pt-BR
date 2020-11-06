---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 3250aa7f9108436cadbf0f46ab0e36d3a9c094d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426886"
---
# <span data-ttu-id="f506b-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f506b-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="f506b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f506b-102">SYNOPSIS</span></span>
<span data-ttu-id="f506b-103">Remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f506b-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f506b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f506b-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f506b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f506b-105">DESCRIPTION</span></span>
<span data-ttu-id="f506b-106">O cmdlet **Remove-AzureRmNetworkInterface** remove uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="f506b-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="f506b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f506b-107">EXAMPLES</span></span>

### <span data-ttu-id="f506b-108">Exemplo 1: remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="f506b-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="f506b-109">Esse comando Remove a interface de NetworkInterface1 na ResourceGroup1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f506b-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="f506b-110">Como o parâmetro *Force* não é usado, o usuário será solicitado a confirmar essa ação.</span><span class="sxs-lookup"><span data-stu-id="f506b-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="f506b-111">Exemplo 2: remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="f506b-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="f506b-112">Esse comando Remove todas as interfaces de rede na ResourceGroup1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f506b-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="f506b-113">Como o parâmetro *Force* é usado, o usuário não será solicitado a confirmar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="f506b-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="f506b-114">OS</span><span class="sxs-lookup"><span data-stu-id="f506b-114">PARAMETERS</span></span>

### <span data-ttu-id="f506b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f506b-115">-Force</span></span>
<span data-ttu-id="f506b-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f506b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f506b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f506b-117">-Name</span></span>
<span data-ttu-id="f506b-118">Especifica o nome da interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f506b-118">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f506b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f506b-119">-PassThru</span></span>
<span data-ttu-id="f506b-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f506b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f506b-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f506b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f506b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f506b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f506b-123">Especifica o nome de um grupo de recursos que contém a interface de rede que esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f506b-123">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f506b-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f506b-124">-Confirm</span></span>
<span data-ttu-id="f506b-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f506b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f506b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f506b-126">-WhatIf</span></span>
<span data-ttu-id="f506b-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f506b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f506b-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f506b-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f506b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f506b-129">-DefaultProfile</span></span>
<span data-ttu-id="f506b-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f506b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f506b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f506b-131">CommonParameters</span></span>
<span data-ttu-id="f506b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f506b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f506b-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f506b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f506b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f506b-134">INPUTS</span></span>

## <span data-ttu-id="f506b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f506b-135">OUTPUTS</span></span>

## <span data-ttu-id="f506b-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f506b-136">NOTES</span></span>

## <span data-ttu-id="f506b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f506b-137">RELATED LINKS</span></span>

[<span data-ttu-id="f506b-138">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f506b-138">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="f506b-139">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f506b-139">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="f506b-140">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f506b-140">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


