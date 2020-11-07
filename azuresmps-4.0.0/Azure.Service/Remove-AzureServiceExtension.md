---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6B5E4968-5DF5-4956-A070-9F54A79D960B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f45e0a93b2f6261ca6031aa721bda3a72f4443dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946113"
---
# <span data-ttu-id="b8f20-101">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="b8f20-101">Remove-AzureServiceExtension</span></span>

## <span data-ttu-id="b8f20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8f20-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f20-103">Remove extensões de serviço de nuvem que são aplicadas em uma implantação.</span><span class="sxs-lookup"><span data-stu-id="b8f20-103">Removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="b8f20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8f20-104">SYNTAX</span></span>

### <span data-ttu-id="b8f20-105">RemoveByRoles (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8f20-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-ExtensionName] <String> [-ProviderNamespace] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b8f20-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="b8f20-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-UninstallConfiguration] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b8f20-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8f20-107">DESCRIPTION</span></span>
<span data-ttu-id="b8f20-108">O cmdlet **Remove-AzureServiceExtension** remove extensões de serviço de nuvem aplicadas em uma implantação.</span><span class="sxs-lookup"><span data-stu-id="b8f20-108">The **Remove-AzureServiceExtension** cmdlet removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="b8f20-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8f20-109">EXAMPLES</span></span>

### <span data-ttu-id="b8f20-110">Exemplo 1: remover uma extensão de serviço</span><span class="sxs-lookup"><span data-stu-id="b8f20-110">Example 1: Remove a service extension</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="b8f20-111">Esse comando Remove uma extensão de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8f20-111">This command removes a service extension.</span></span>

### <span data-ttu-id="b8f20-112">Exemplo 2: remover uma extensão de serviço e desinstalar todas as configurações</span><span class="sxs-lookup"><span data-stu-id="b8f20-112">Example 2: Remove a service extension and uninstall all configurations</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -UninstallConfiguration
```

<span data-ttu-id="b8f20-113">Esse comando Remove uma extensão de serviço e desinstala todas as configurações.</span><span class="sxs-lookup"><span data-stu-id="b8f20-113">This command removes a service extension and uninstalls all configurations.</span></span>

## <span data-ttu-id="b8f20-114">OS</span><span class="sxs-lookup"><span data-stu-id="b8f20-114">PARAMETERS</span></span>

### <span data-ttu-id="b8f20-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="b8f20-115">-ExtensionName</span></span>
<span data-ttu-id="b8f20-116">Especifica o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="b8f20-116">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8f20-117">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b8f20-117">-InformationAction</span></span>
<span data-ttu-id="b8f20-118">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b8f20-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8f20-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b8f20-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8f20-120">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b8f20-120">Continue</span></span>
- <span data-ttu-id="b8f20-121">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b8f20-121">Ignore</span></span>
- <span data-ttu-id="b8f20-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="b8f20-122">Inquire</span></span>
- <span data-ttu-id="b8f20-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b8f20-123">SilentlyContinue</span></span>
- <span data-ttu-id="b8f20-124">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b8f20-124">Stop</span></span>
- <span data-ttu-id="b8f20-125">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b8f20-125">Suspend</span></span>

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

### <span data-ttu-id="b8f20-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b8f20-126">-InformationVariable</span></span>
<span data-ttu-id="b8f20-127">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b8f20-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b8f20-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b8f20-128">-Profile</span></span>
<span data-ttu-id="b8f20-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b8f20-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8f20-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b8f20-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8f20-131">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="b8f20-131">-ProviderNamespace</span></span>
<span data-ttu-id="b8f20-132">Especifica o namespace do provedor de extensão.</span><span class="sxs-lookup"><span data-stu-id="b8f20-132">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8f20-133">-Função</span><span class="sxs-lookup"><span data-stu-id="b8f20-133">-Role</span></span>
<span data-ttu-id="b8f20-134">Especifica uma matriz opcional de funções para especificar a extensão.</span><span class="sxs-lookup"><span data-stu-id="b8f20-134">Specifies an optional array of roles to specify the extension for.</span></span>
<span data-ttu-id="b8f20-135">Se não especificado, a extensão será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="b8f20-135">If not specified the extension is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="b8f20-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b8f20-136">-ServiceName</span></span>
<span data-ttu-id="b8f20-137">Especifica o nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b8f20-137">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="b8f20-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="b8f20-138">-Slot</span></span>
<span data-ttu-id="b8f20-139">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="b8f20-139">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="b8f20-140">Os valores válidos são produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="b8f20-140">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="b8f20-141">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8f20-141">-UninstallConfiguration</span></span>
<span data-ttu-id="b8f20-142">Indica que esse cmdlet desinstala todas as configurações do serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b8f20-142">Indicates that this cmdlet uninstalls all configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8f20-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f20-143">CommonParameters</span></span>
<span data-ttu-id="b8f20-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8f20-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f20-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8f20-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f20-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8f20-146">INPUTS</span></span>

## <span data-ttu-id="b8f20-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8f20-147">OUTPUTS</span></span>

## <span data-ttu-id="b8f20-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8f20-148">NOTES</span></span>

## <span data-ttu-id="b8f20-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8f20-149">RELATED LINKS</span></span>

[<span data-ttu-id="b8f20-150">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="b8f20-150">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="b8f20-151">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="b8f20-151">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


