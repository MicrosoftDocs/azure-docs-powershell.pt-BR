---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946126"
---
# <span data-ttu-id="31ee0-101">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="31ee0-101">Remove-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="31ee0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="31ee0-103">Remove a extensão de domínio do AD do serviço de nuvem aplicada a todas as funções ou funções nomeadas em um determinado slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="31ee0-103">Removes the cloud service AD domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="31ee0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31ee0-104">SYNTAX</span></span>

### <span data-ttu-id="31ee0-105">RemoveByRoles (padrão)</span><span class="sxs-lookup"><span data-stu-id="31ee0-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="31ee0-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="31ee0-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="31ee0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31ee0-107">DESCRIPTION</span></span>
<span data-ttu-id="31ee0-108">O cmdlet **Remove-AzureServiceADDomainExtension** remove a extensão de domínio do serviço de nuvem do Active Directory (AD) aplicada a todas as funções ou funções nomeadas em um determinado slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="31ee0-108">The **Remove-AzureServiceADDomainExtension** cmdlet removes the cloud service Active Directory (AD) domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="31ee0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31ee0-109">EXAMPLES</span></span>

### <span data-ttu-id="31ee0-110">Exemplo 1: remover uma extensão de domínio do AD</span><span class="sxs-lookup"><span data-stu-id="31ee0-110">Example 1: Remove an AD domain extension</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="31ee0-111">Esse comando Remove a extensão especificada pela variável $Svc.</span><span class="sxs-lookup"><span data-stu-id="31ee0-111">This command removes the extension specified by the $Svc variable.</span></span>

### <span data-ttu-id="31ee0-112">Exemplo 2: remover uma extensão de domínio do AD para uma função especificada</span><span class="sxs-lookup"><span data-stu-id="31ee0-112">Example 2: Remove an AD Domain extension for a specified role</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

<span data-ttu-id="31ee0-113">Esse comando Remove a extensão de serviço da função especificada.</span><span class="sxs-lookup"><span data-stu-id="31ee0-113">This command removes the service extension for the specified role.</span></span>

## <span data-ttu-id="31ee0-114">OS</span><span class="sxs-lookup"><span data-stu-id="31ee0-114">PARAMETERS</span></span>

### <span data-ttu-id="31ee0-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="31ee0-115">-InformationAction</span></span>
<span data-ttu-id="31ee0-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="31ee0-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="31ee0-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="31ee0-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31ee0-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="31ee0-118">Continue</span></span>
- <span data-ttu-id="31ee0-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="31ee0-119">Ignore</span></span>
- <span data-ttu-id="31ee0-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="31ee0-120">Inquire</span></span>
- <span data-ttu-id="31ee0-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="31ee0-121">SilentlyContinue</span></span>
- <span data-ttu-id="31ee0-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="31ee0-122">Stop</span></span>
- <span data-ttu-id="31ee0-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="31ee0-123">Suspend</span></span>

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

### <span data-ttu-id="31ee0-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="31ee0-124">-InformationVariable</span></span>
<span data-ttu-id="31ee0-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="31ee0-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="31ee0-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="31ee0-126">-Profile</span></span>
<span data-ttu-id="31ee0-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="31ee0-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31ee0-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="31ee0-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="31ee0-129">-Função</span><span class="sxs-lookup"><span data-stu-id="31ee0-129">-Role</span></span>
<span data-ttu-id="31ee0-130">Especifica uma matriz opcional de funções para as quais especificar a configuração da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="31ee0-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="31ee0-131">Se não for especificado, a configuração de domínio do AD será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="31ee0-131">If not specified, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ee0-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="31ee0-132">-ServiceName</span></span>
<span data-ttu-id="31ee0-133">Especifica o nome de um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="31ee0-133">Specifies the name of an Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ee0-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="31ee0-134">-Slot</span></span>
<span data-ttu-id="31ee0-135">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="31ee0-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="31ee0-136">Os valores válidos são: produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="31ee0-136">Valid values are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ee0-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="31ee0-137">-UninstallConfiguration</span></span>
<span data-ttu-id="31ee0-138">Indica que esse cmdlet desinstala todas as configurações de domínio do AD do serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="31ee0-138">Indicates that this cmdlet uninstalls all AD domain configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ee0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ee0-139">CommonParameters</span></span>
<span data-ttu-id="31ee0-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ee0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ee0-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ee0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ee0-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31ee0-142">INPUTS</span></span>

## <span data-ttu-id="31ee0-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31ee0-143">OUTPUTS</span></span>

## <span data-ttu-id="31ee0-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31ee0-144">NOTES</span></span>

## <span data-ttu-id="31ee0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31ee0-145">RELATED LINKS</span></span>

[<span data-ttu-id="31ee0-146">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="31ee0-146">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="31ee0-147">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="31ee0-147">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


