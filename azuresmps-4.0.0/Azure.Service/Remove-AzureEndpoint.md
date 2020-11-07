---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5A068EC9-3745-4219-BA03-C56CB9D9D157
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24fad9fc499c3f7abec5e7539fd1e221835849ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946478"
---
# <span data-ttu-id="b65df-101">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b65df-101">Remove-AzureEndpoint</span></span>

## <span data-ttu-id="b65df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b65df-102">SYNOPSIS</span></span>
<span data-ttu-id="b65df-103">Exclui um ponto de extremidade de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="b65df-103">Deletes an endpoint from an Azure virtual machine.</span></span>

## <span data-ttu-id="b65df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b65df-104">SYNTAX</span></span>

```
Remove-AzureEndpoint [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b65df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b65df-105">DESCRIPTION</span></span>
<span data-ttu-id="b65df-106">O cmdlet **Remove-AzureEndpoint** exclui um ponto de extremidade de um objeto de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="b65df-106">The **Remove-AzureEndpoint** cmdlet deletes an endpoint from an Azure virtual machine object.</span></span>

## <span data-ttu-id="b65df-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b65df-107">EXAMPLES</span></span>

### <span data-ttu-id="b65df-108">Exemplo 1: remover um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="b65df-108">Example 1: Remove an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine01" | Remove-AzureEndpoint -Name "HttpIn" | Update-AzureVM
```

<span data-ttu-id="b65df-109">Esse comando recupera a configuração de uma máquina virtual nomeada VirtualMachine01 usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="b65df-109">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="b65df-110">O comando passa a ele para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="b65df-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b65df-111">Esse cmdlet Remove um ponto de extremidade chamado Httpem.</span><span class="sxs-lookup"><span data-stu-id="b65df-111">This cmdlet removes an endpoint named HttpIn.</span></span>
<span data-ttu-id="b65df-112">O comando passa o objeto da máquina virtual para o cmdlet **Update-AzureVM** , que implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="b65df-112">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="b65df-113">OS</span><span class="sxs-lookup"><span data-stu-id="b65df-113">PARAMETERS</span></span>

### <span data-ttu-id="b65df-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b65df-114">-InformationAction</span></span>
<span data-ttu-id="b65df-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b65df-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b65df-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b65df-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b65df-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b65df-117">Continue</span></span>
- <span data-ttu-id="b65df-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b65df-118">Ignore</span></span>
- <span data-ttu-id="b65df-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="b65df-119">Inquire</span></span>
- <span data-ttu-id="b65df-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b65df-120">SilentlyContinue</span></span>
- <span data-ttu-id="b65df-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b65df-121">Stop</span></span>
- <span data-ttu-id="b65df-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b65df-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65df-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b65df-123">-InformationVariable</span></span>
<span data-ttu-id="b65df-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b65df-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65df-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b65df-125">-Name</span></span>
<span data-ttu-id="b65df-126">Especifica o nome do ponto de extremidade que este cmdlet exclui da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b65df-126">Specifies the name of the endpoint that this cmdlet deletes from the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65df-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b65df-127">-Profile</span></span>
<span data-ttu-id="b65df-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b65df-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b65df-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b65df-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65df-130">-VM</span><span class="sxs-lookup"><span data-stu-id="b65df-130">-VM</span></span>
<span data-ttu-id="b65df-131">Especifica a máquina virtual a partir da qual esse cmdlet exclui um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b65df-131">Specifies the virtual machine from which this cmdlet deletes an endpoint.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b65df-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65df-132">CommonParameters</span></span>
<span data-ttu-id="b65df-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b65df-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65df-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b65df-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65df-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b65df-135">INPUTS</span></span>

## <span data-ttu-id="b65df-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b65df-136">OUTPUTS</span></span>

## <span data-ttu-id="b65df-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b65df-137">NOTES</span></span>

## <span data-ttu-id="b65df-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b65df-138">RELATED LINKS</span></span>

[<span data-ttu-id="b65df-139">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b65df-139">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="b65df-140">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b65df-140">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="b65df-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b65df-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="b65df-142">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b65df-142">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="b65df-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b65df-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


