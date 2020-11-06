---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 60c6a106acec84b3f43a3bd825e7be9b87fe8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440113"
---
# <span data-ttu-id="fcc6a-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fcc6a-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="fcc6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcc6a-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc6a-103">Remove um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcc6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcc6a-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcc6a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcc6a-105">DESCRIPTION</span></span>
<span data-ttu-id="fcc6a-106">O cmdlet **Remove-AzureRmPublicIpAddress** remove um endereço IP público do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="fcc6a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcc6a-107">EXAMPLES</span></span>

### <span data-ttu-id="fcc6a-108">1: remover um recurso de endereço IP público</span><span class="sxs-lookup"><span data-stu-id="fcc6a-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="fcc6a-109">Este comando Remove o recurso de endereço IP público chamado $publicIpName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="fcc6a-110">OS</span><span class="sxs-lookup"><span data-stu-id="fcc6a-110">PARAMETERS</span></span>

### <span data-ttu-id="fcc6a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcc6a-111">-AsJob</span></span>
<span data-ttu-id="fcc6a-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fcc6a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fcc6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc6a-113">-DefaultProfile</span></span>
<span data-ttu-id="fcc6a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcc6a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fcc6a-115">-Force</span></span>
<span data-ttu-id="fcc6a-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fcc6a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcc6a-117">-Name</span></span>
<span data-ttu-id="fcc6a-118">Especifica o nome do endereço IP público que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fcc6a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcc6a-119">-PassThru</span></span>
<span data-ttu-id="fcc6a-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fcc6a-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fcc6a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc6a-122">-ResourceGroupName</span></span>
<span data-ttu-id="fcc6a-123">Especifica o nome do grupo de recursos que contém o endereço IP público que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fcc6a-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fcc6a-124">-Confirm</span></span>
<span data-ttu-id="fcc6a-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcc6a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcc6a-126">-WhatIf</span></span>
<span data-ttu-id="fcc6a-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcc6a-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcc6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc6a-129">CommonParameters</span></span>
<span data-ttu-id="fcc6a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc6a-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc6a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc6a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcc6a-132">INPUTS</span></span>

### <span data-ttu-id="fcc6a-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fcc6a-133">None</span></span>
<span data-ttu-id="fcc6a-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fcc6a-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcc6a-135">OUTPUTS</span></span>

## <span data-ttu-id="fcc6a-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcc6a-136">NOTES</span></span>

## <span data-ttu-id="fcc6a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcc6a-137">RELATED LINKS</span></span>

[<span data-ttu-id="fcc6a-138">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fcc6a-138">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="fcc6a-139">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fcc6a-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="fcc6a-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fcc6a-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


