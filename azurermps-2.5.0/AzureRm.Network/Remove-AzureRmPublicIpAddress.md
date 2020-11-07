---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: af8a85c698a59a31516c6dee05bb57415a45ff62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785655"
---
# <span data-ttu-id="bdf4c-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf4c-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="bdf4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdf4c-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf4c-103">Remove um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdf4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdf4c-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdf4c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdf4c-105">DESCRIPTION</span></span>
<span data-ttu-id="bdf4c-106">O cmdlet **Remove-AzureRmPublicIpAddress** remove um endereço IP público do Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="bdf4c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdf4c-107">EXAMPLES</span></span>

### <span data-ttu-id="bdf4c-108">1: remover um recurso de endereço IP público</span><span class="sxs-lookup"><span data-stu-id="bdf4c-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="bdf4c-109">Este comando Remove o recurso de endereço IP público chamado $publicIpName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="bdf4c-110">OS</span><span class="sxs-lookup"><span data-stu-id="bdf4c-110">PARAMETERS</span></span>

### <span data-ttu-id="bdf4c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdf4c-111">-AsJob</span></span>
<span data-ttu-id="bdf4c-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bdf4c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdf4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf4c-113">-DefaultProfile</span></span>
<span data-ttu-id="bdf4c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdf4c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bdf4c-115">-Force</span></span>
<span data-ttu-id="bdf4c-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bdf4c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdf4c-117">-Name</span></span>
<span data-ttu-id="bdf4c-118">Especifica o nome do endereço IP público que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bdf4c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdf4c-119">-PassThru</span></span>
<span data-ttu-id="bdf4c-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bdf4c-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bdf4c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdf4c-122">-ResourceGroupName</span></span>
<span data-ttu-id="bdf4c-123">Especifica o nome do grupo de recursos que contém o endereço IP público que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bdf4c-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bdf4c-124">-Confirm</span></span>
<span data-ttu-id="bdf4c-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdf4c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdf4c-126">-WhatIf</span></span>
<span data-ttu-id="bdf4c-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdf4c-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdf4c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf4c-129">CommonParameters</span></span>
<span data-ttu-id="bdf4c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf4c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf4c-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdf4c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf4c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdf4c-132">INPUTS</span></span>

## <span data-ttu-id="bdf4c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdf4c-133">OUTPUTS</span></span>

## <span data-ttu-id="bdf4c-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdf4c-134">NOTES</span></span>

## <span data-ttu-id="bdf4c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdf4c-135">RELATED LINKS</span></span>

[<span data-ttu-id="bdf4c-136">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf4c-136">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="bdf4c-137">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf4c-137">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="bdf4c-138">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf4c-138">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


