---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
ms.openlocfilehash: 1a6c5ae69ef6aa6dc0f64d118fcbc733c97e23a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429440"
---
# <span data-ttu-id="2d03a-101">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2d03a-101">Remove-AzureRmFirewall</span></span>

## <span data-ttu-id="2d03a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d03a-102">SYNOPSIS</span></span>
<span data-ttu-id="2d03a-103">Remover um firewall.</span><span class="sxs-lookup"><span data-stu-id="2d03a-103">Remove a Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d03a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d03a-104">SYNTAX</span></span>

```
Remove-AzureRmFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d03a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d03a-105">DESCRIPTION</span></span>
<span data-ttu-id="2d03a-106">O cmdlet **Remove-AzureRmFirewall** remove um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d03a-106">The **Remove-AzureRmFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="2d03a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d03a-107">EXAMPLES</span></span>

### <span data-ttu-id="2d03a-108">1: criar e excluir um firewall</span><span class="sxs-lookup"><span data-stu-id="2d03a-108">1: Create and delete a Firewall</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="2d03a-109">Este exemplo cria um firewall e, em seguida, o exclui.</span><span class="sxs-lookup"><span data-stu-id="2d03a-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="2d03a-110">Para suprimir o prompt ao excluir o firewall, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="2d03a-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="2d03a-111">2: desatribuir o firewall e excluir o firewall</span><span class="sxs-lookup"><span data-stu-id="2d03a-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzureRmFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="2d03a-112">Este exemplo recupera um firewall, desatribui o firewall e exclui o firewall.</span><span class="sxs-lookup"><span data-stu-id="2d03a-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="2d03a-113">O comando DEALLOCATE remove o serviço em execução, mas preserva a configuração do firewall.</span><span class="sxs-lookup"><span data-stu-id="2d03a-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="2d03a-114">Se o usuário quiser iniciar o serviço novamente, o método de alocação deve ser chamado no firewall.</span><span class="sxs-lookup"><span data-stu-id="2d03a-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="2d03a-115">Para suprimir o prompt ao excluir o firewall, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="2d03a-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="2d03a-116">OS</span><span class="sxs-lookup"><span data-stu-id="2d03a-116">PARAMETERS</span></span>

### <span data-ttu-id="2d03a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d03a-117">-AsJob</span></span>
<span data-ttu-id="2d03a-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2d03a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d03a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d03a-119">-DefaultProfile</span></span>
<span data-ttu-id="2d03a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d03a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d03a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2d03a-121">-Force</span></span>
<span data-ttu-id="2d03a-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2d03a-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d03a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d03a-123">-Name</span></span>
<span data-ttu-id="2d03a-124">Especifica o nome do firewall que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="2d03a-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2d03a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d03a-125">-PassThru</span></span>
<span data-ttu-id="2d03a-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="2d03a-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2d03a-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="2d03a-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d03a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d03a-128">-ResourceGroupName</span></span>
<span data-ttu-id="2d03a-129">Especifica o nome do grupo de recursos que contém o firewall que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="2d03a-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2d03a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2d03a-130">-Confirm</span></span>
<span data-ttu-id="2d03a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d03a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d03a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d03a-132">-WhatIf</span></span>
<span data-ttu-id="2d03a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d03a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d03a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d03a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d03a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d03a-135">CommonParameters</span></span>
<span data-ttu-id="2d03a-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d03a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d03a-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d03a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d03a-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d03a-138">INPUTS</span></span>

### <span data-ttu-id="2d03a-139">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2d03a-139">PSAzureFirewall</span></span>
<span data-ttu-id="2d03a-140">O tipo ' PSAzureFirewall ' é aceito da pipeline</span><span class="sxs-lookup"><span data-stu-id="2d03a-140">Type 'PSAzureFirewall' is accepted from the pipeline</span></span>

## <span data-ttu-id="2d03a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d03a-141">OUTPUTS</span></span>

## <span data-ttu-id="2d03a-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d03a-142">NOTES</span></span>

## <span data-ttu-id="2d03a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d03a-143">RELATED LINKS</span></span>

[<span data-ttu-id="2d03a-144">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2d03a-144">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="2d03a-145">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2d03a-145">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="2d03a-146">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2d03a-146">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
