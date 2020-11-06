---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: b0387d10950073c4655c6e6015edc6957ae14edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430733"
---
# <span data-ttu-id="b34ed-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b34ed-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="b34ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b34ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b34ed-103">Remove um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b34ed-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b34ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b34ed-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b34ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b34ed-105">DESCRIPTION</span></span>
<span data-ttu-id="b34ed-106">O cmdlet **Remove-AzureRmApplicationSecurityGroup** remove um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b34ed-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="b34ed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b34ed-107">EXAMPLES</span></span>

### <span data-ttu-id="b34ed-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b34ed-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b34ed-109">Esse comando exclui um grupo de segurança de aplicativo chamado MyApplicationSecurityGrouo no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="b34ed-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="b34ed-110">OS</span><span class="sxs-lookup"><span data-stu-id="b34ed-110">PARAMETERS</span></span>

### <span data-ttu-id="b34ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34ed-111">-DefaultProfile</span></span>
<span data-ttu-id="b34ed-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b34ed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b34ed-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b34ed-113">-Force</span></span>
<span data-ttu-id="b34ed-114">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="b34ed-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="b34ed-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b34ed-115">-Name</span></span>
<span data-ttu-id="b34ed-116">O nome do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b34ed-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="b34ed-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b34ed-117">-PassThru</span></span>
<span data-ttu-id="b34ed-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b34ed-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b34ed-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b34ed-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b34ed-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34ed-120">-ResourceGroupName</span></span>
<span data-ttu-id="b34ed-121">O nome do grupo de recursos do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b34ed-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="b34ed-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b34ed-122">-Confirm</span></span>
<span data-ttu-id="b34ed-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b34ed-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b34ed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b34ed-124">-WhatIf</span></span>
<span data-ttu-id="b34ed-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b34ed-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b34ed-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b34ed-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b34ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34ed-127">CommonParameters</span></span>
<span data-ttu-id="b34ed-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34ed-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34ed-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34ed-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b34ed-130">INPUTS</span></span>

### <span data-ttu-id="b34ed-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b34ed-131">System.String</span></span>

## <span data-ttu-id="b34ed-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b34ed-132">OUTPUTS</span></span>

### <span data-ttu-id="b34ed-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="b34ed-133">System.Object</span></span>

## <span data-ttu-id="b34ed-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b34ed-134">NOTES</span></span>

## <span data-ttu-id="b34ed-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b34ed-135">RELATED LINKS</span></span>

[<span data-ttu-id="b34ed-136">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b34ed-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="b34ed-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b34ed-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
