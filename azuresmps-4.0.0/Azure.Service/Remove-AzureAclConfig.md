---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946175"
---
# <span data-ttu-id="6475c-101">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6475c-101">Remove-AzureAclConfig</span></span>

## <span data-ttu-id="6475c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6475c-102">SYNOPSIS</span></span>
<span data-ttu-id="6475c-103">Remove um objeto de configuração ACL de uma configuração de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6475c-103">Removes an ACL configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="6475c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6475c-104">SYNTAX</span></span>

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6475c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6475c-105">DESCRIPTION</span></span>
<span data-ttu-id="6475c-106">O cmdlet **Remove-AzureAclConfig** remove um objeto de configuração de ACL (lista de controle de acesso) de uma configuração de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6475c-106">The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="6475c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6475c-107">EXAMPLES</span></span>

### <span data-ttu-id="6475c-108">Exemplo 1: remover uma configuração de ACL</span><span class="sxs-lookup"><span data-stu-id="6475c-108">Example 1: Remove an ACL configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

<span data-ttu-id="6475c-109">Esse comando obtém a máquina virtual chamada VirtualMachine07 no serviço chamado ContosoService usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="6475c-109">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="6475c-110">O comando passa o objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="6475c-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6475c-111">Esse cmdlet Remove a configuração de ACL para o ponto de extremidade chamado Web.</span><span class="sxs-lookup"><span data-stu-id="6475c-111">That cmdlet removes the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="6475c-112">O comando passa o resultado para o cmdlet **Update-AzureVM** , que atualiza a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6475c-112">The command passes the result to the **Update-AzureVM** cmdlet, which updates the virtual machine.</span></span>

## <span data-ttu-id="6475c-113">OS</span><span class="sxs-lookup"><span data-stu-id="6475c-113">PARAMETERS</span></span>

### <span data-ttu-id="6475c-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6475c-114">-EndpointName</span></span>
<span data-ttu-id="6475c-115">Especifica o nome do ponto de extremidade do qual esse cmdlet Remove a configuração de ACL.</span><span class="sxs-lookup"><span data-stu-id="6475c-115">Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.</span></span>

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

### <span data-ttu-id="6475c-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6475c-116">-InformationAction</span></span>
<span data-ttu-id="6475c-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="6475c-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6475c-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6475c-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6475c-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="6475c-119">Continue</span></span>
- <span data-ttu-id="6475c-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="6475c-120">Ignore</span></span>
- <span data-ttu-id="6475c-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="6475c-121">Inquire</span></span>
- <span data-ttu-id="6475c-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6475c-122">SilentlyContinue</span></span>
- <span data-ttu-id="6475c-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="6475c-123">Stop</span></span>
- <span data-ttu-id="6475c-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="6475c-124">Suspend</span></span>

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

### <span data-ttu-id="6475c-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6475c-125">-InformationVariable</span></span>
<span data-ttu-id="6475c-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="6475c-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6475c-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6475c-127">-Profile</span></span>
<span data-ttu-id="6475c-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6475c-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6475c-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6475c-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6475c-130">-VM</span><span class="sxs-lookup"><span data-stu-id="6475c-130">-VM</span></span>
<span data-ttu-id="6475c-131">Especifica a máquina virtual a partir da qual esse cmdlet Remove uma configuração de ACL.</span><span class="sxs-lookup"><span data-stu-id="6475c-131">Specifies the virtual machine from which this cmdlet removes an ACL configuration.</span></span>

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

### <span data-ttu-id="6475c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6475c-132">CommonParameters</span></span>
<span data-ttu-id="6475c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6475c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6475c-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6475c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6475c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6475c-135">INPUTS</span></span>

## <span data-ttu-id="6475c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6475c-136">OUTPUTS</span></span>

## <span data-ttu-id="6475c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6475c-137">NOTES</span></span>

## <span data-ttu-id="6475c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6475c-138">RELATED LINKS</span></span>

[<span data-ttu-id="6475c-139">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6475c-139">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="6475c-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6475c-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="6475c-141">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6475c-141">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="6475c-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6475c-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)

[<span data-ttu-id="6475c-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6475c-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


