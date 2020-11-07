---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945673"
---
# <span data-ttu-id="7521a-101">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="7521a-101">Get-AzureAclConfig</span></span>

## <span data-ttu-id="7521a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7521a-102">SYNOPSIS</span></span>
<span data-ttu-id="7521a-103">Obtém o objeto de configuração ACL de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7521a-103">Gets the ACL configuration object from an Azure virtual machine.</span></span>

## <span data-ttu-id="7521a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7521a-104">SYNTAX</span></span>

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7521a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7521a-105">DESCRIPTION</span></span>
<span data-ttu-id="7521a-106">O cmdlet **Get-AzureAclConfig** Obtém o objeto de configuração ACL (lista de controle de acesso) de uma máquina virtual do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="7521a-106">The **Get-AzureAclConfig** cmdlet gets the access control list (ACL) configuration object from an existing Azure virtual machine.</span></span>

## <span data-ttu-id="7521a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7521a-107">EXAMPLES</span></span>

### <span data-ttu-id="7521a-108">Exemplo 1: obter um objeto de configuração de ACL para um ponto de extremidade de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7521a-108">Example 1: Get an ACL configuration object for a virtual machine endpoint</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

<span data-ttu-id="7521a-109">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 no serviço chamado ContosoService usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="7521a-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="7521a-110">O comando passa esse objeto para o cmdlet **Get-AzureAclConfig** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="7521a-110">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7521a-111">Esse cmdlet obtém a configuração de ACL para o ponto de extremidade chamado Web.</span><span class="sxs-lookup"><span data-stu-id="7521a-111">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="7521a-112">O comando armazena esse objeto de configuração de ACL na variável $Acl.</span><span class="sxs-lookup"><span data-stu-id="7521a-112">The command stores that ACL configuration object in the $Acl variable.</span></span>

## <span data-ttu-id="7521a-113">OS</span><span class="sxs-lookup"><span data-stu-id="7521a-113">PARAMETERS</span></span>

### <span data-ttu-id="7521a-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7521a-114">-EndpointName</span></span>
<span data-ttu-id="7521a-115">Especifica o nome do ponto de extremidade para o qual esse cmdlet obtém uma ACL.</span><span class="sxs-lookup"><span data-stu-id="7521a-115">Specifies the name of the endpoint for which this cmdlet gets an ACL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7521a-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="7521a-116">-InformationAction</span></span>
<span data-ttu-id="7521a-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="7521a-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7521a-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7521a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7521a-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="7521a-119">Continue</span></span>
- <span data-ttu-id="7521a-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="7521a-120">Ignore</span></span>
- <span data-ttu-id="7521a-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="7521a-121">Inquire</span></span>
- <span data-ttu-id="7521a-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7521a-122">SilentlyContinue</span></span>
- <span data-ttu-id="7521a-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="7521a-123">Stop</span></span>
- <span data-ttu-id="7521a-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="7521a-124">Suspend</span></span>

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

### <span data-ttu-id="7521a-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7521a-125">-InformationVariable</span></span>
<span data-ttu-id="7521a-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="7521a-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7521a-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7521a-127">-Profile</span></span>
<span data-ttu-id="7521a-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7521a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7521a-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7521a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7521a-130">-VM</span><span class="sxs-lookup"><span data-stu-id="7521a-130">-VM</span></span>
<span data-ttu-id="7521a-131">Especifica o objeto da máquina virtual para o qual este cmdlet obtém a configuração de ACL.</span><span class="sxs-lookup"><span data-stu-id="7521a-131">Specifies the virtual machine object for which this cmdlet gets ACL configuration.</span></span>

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

### <span data-ttu-id="7521a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7521a-132">CommonParameters</span></span>
<span data-ttu-id="7521a-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7521a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7521a-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7521a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7521a-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7521a-135">INPUTS</span></span>

## <span data-ttu-id="7521a-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7521a-136">OUTPUTS</span></span>

## <span data-ttu-id="7521a-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7521a-137">NOTES</span></span>

## <span data-ttu-id="7521a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7521a-138">RELATED LINKS</span></span>

[<span data-ttu-id="7521a-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7521a-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="7521a-140">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="7521a-140">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="7521a-141">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="7521a-141">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="7521a-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="7521a-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


