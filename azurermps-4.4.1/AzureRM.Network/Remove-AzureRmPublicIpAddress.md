---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 396f603c4a4126b8d438f0048677da7a5dbd7492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430726"
---
# <span data-ttu-id="64266-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="64266-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="64266-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64266-102">SYNOPSIS</span></span>
<span data-ttu-id="64266-103">Remove um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="64266-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64266-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64266-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64266-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64266-105">DESCRIPTION</span></span>
<span data-ttu-id="64266-106">O cmdlet **Remove-AzureRmPublicIpAddress** remove um endereço IP público do Azure.</span><span class="sxs-lookup"><span data-stu-id="64266-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="64266-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64266-107">EXAMPLES</span></span>

### <span data-ttu-id="64266-108">1: remover um recurso de endereço IP público</span><span class="sxs-lookup"><span data-stu-id="64266-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="64266-109">Este comando Remove o recurso de endereço IP público chamado $publicIpName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64266-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="64266-110">OS</span><span class="sxs-lookup"><span data-stu-id="64266-110">PARAMETERS</span></span>

### <span data-ttu-id="64266-111">-Force</span><span class="sxs-lookup"><span data-stu-id="64266-111">-Force</span></span>
<span data-ttu-id="64266-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="64266-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64266-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="64266-113">-Name</span></span>
<span data-ttu-id="64266-114">Especifica o nome do endereço IP público que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="64266-114">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="64266-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64266-115">-PassThru</span></span>
<span data-ttu-id="64266-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="64266-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="64266-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="64266-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="64266-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64266-118">-ResourceGroupName</span></span>
<span data-ttu-id="64266-119">Especifica o nome do grupo de recursos que contém o endereço IP público que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="64266-119">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="64266-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64266-120">-Confirm</span></span>
<span data-ttu-id="64266-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64266-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64266-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64266-122">-WhatIf</span></span>
<span data-ttu-id="64266-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64266-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64266-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64266-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64266-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64266-125">-DefaultProfile</span></span>
<span data-ttu-id="64266-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64266-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64266-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64266-127">CommonParameters</span></span>
<span data-ttu-id="64266-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64266-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64266-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64266-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64266-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64266-130">INPUTS</span></span>

## <span data-ttu-id="64266-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64266-131">OUTPUTS</span></span>

## <span data-ttu-id="64266-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64266-132">NOTES</span></span>

## <span data-ttu-id="64266-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64266-133">RELATED LINKS</span></span>

[<span data-ttu-id="64266-134">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="64266-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="64266-135">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="64266-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="64266-136">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="64266-136">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


