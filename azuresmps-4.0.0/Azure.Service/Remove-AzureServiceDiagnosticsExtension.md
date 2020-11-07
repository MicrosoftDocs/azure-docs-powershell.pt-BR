---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946116"
---
# <span data-ttu-id="caf79-101">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="caf79-101">Remove-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="caf79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="caf79-102">SYNOPSIS</span></span>
<span data-ttu-id="caf79-103">Remove a extensão de diagnóstico do serviço na nuvem aplicada a todas as funções ou funções nomeadas em um determinado slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="caf79-103">Removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="caf79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="caf79-104">SYNTAX</span></span>

### <span data-ttu-id="caf79-105">RemoveByRoles (padrão)</span><span class="sxs-lookup"><span data-stu-id="caf79-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="caf79-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="caf79-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="caf79-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="caf79-107">DESCRIPTION</span></span>
<span data-ttu-id="caf79-108">O cmdlet **Remove-AzureServiceDiagnosticsExtension** remove a extensão do diagnóstico do serviço em nuvem aplicada a todas as funções ou funções nomeadas em um determinado slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="caf79-108">The **Remove-AzureServiceDiagnosticsExtension** cmdlet removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="caf79-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="caf79-109">EXAMPLES</span></span>

### <span data-ttu-id="caf79-110">Exemplo 1: remover a extensão de diagnóstico de um serviço</span><span class="sxs-lookup"><span data-stu-id="caf79-110">Example 1: Remove the diagnostic extension for a service</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="caf79-111">Este comando Remove a extensão de diagnóstico de uma função especificada.</span><span class="sxs-lookup"><span data-stu-id="caf79-111">This command removes the diagnostic extension for a specified role.</span></span>

### <span data-ttu-id="caf79-112">Exemplo 2: remover a extensão de diagnóstico de um serviço em uma função especificada</span><span class="sxs-lookup"><span data-stu-id="caf79-112">Example 2: Remove the diagnostic extension for a service in a specified role</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

<span data-ttu-id="caf79-113">Este comando Remove a extensão de diagnóstico de uma função especificada.</span><span class="sxs-lookup"><span data-stu-id="caf79-113">This command removes the diagnostic extension for a specified role.</span></span>

## <span data-ttu-id="caf79-114">OS</span><span class="sxs-lookup"><span data-stu-id="caf79-114">PARAMETERS</span></span>

### <span data-ttu-id="caf79-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="caf79-115">-InformationAction</span></span>
<span data-ttu-id="caf79-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="caf79-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="caf79-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="caf79-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="caf79-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="caf79-118">Continue</span></span>
- <span data-ttu-id="caf79-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="caf79-119">Ignore</span></span>
- <span data-ttu-id="caf79-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="caf79-120">Inquire</span></span>
- <span data-ttu-id="caf79-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="caf79-121">SilentlyContinue</span></span>
- <span data-ttu-id="caf79-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="caf79-122">Stop</span></span>
- <span data-ttu-id="caf79-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="caf79-123">Suspend</span></span>

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

### <span data-ttu-id="caf79-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="caf79-124">-InformationVariable</span></span>
<span data-ttu-id="caf79-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="caf79-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="caf79-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="caf79-126">-Profile</span></span>
<span data-ttu-id="caf79-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="caf79-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="caf79-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="caf79-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="caf79-129">-Função</span><span class="sxs-lookup"><span data-stu-id="caf79-129">-Role</span></span>
<span data-ttu-id="caf79-130">Especifica uma matriz opcional de funções para as quais especificar a configuração da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="caf79-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="caf79-131">Se você não especificar esse parâmetro, a configuração da área de trabalho remota será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="caf79-131">If you do not specify this parameter, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="caf79-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="caf79-132">-ServiceName</span></span>
<span data-ttu-id="caf79-133">Especifica o nome do serviço do Azure da implantação.</span><span class="sxs-lookup"><span data-stu-id="caf79-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="caf79-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="caf79-134">-Slot</span></span>
<span data-ttu-id="caf79-135">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="caf79-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="caf79-136">Os valores válidos são produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="caf79-136">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="caf79-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="caf79-137">-UninstallConfiguration</span></span>
<span data-ttu-id="caf79-138">Indica que esse cmdlet desinstala todas as configurações de RDP do serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="caf79-138">Indicates that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="caf79-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf79-139">CommonParameters</span></span>
<span data-ttu-id="caf79-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caf79-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf79-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf79-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf79-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="caf79-142">INPUTS</span></span>

## <span data-ttu-id="caf79-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="caf79-143">OUTPUTS</span></span>

## <span data-ttu-id="caf79-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="caf79-144">NOTES</span></span>

## <span data-ttu-id="caf79-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="caf79-145">RELATED LINKS</span></span>

[<span data-ttu-id="caf79-146">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="caf79-146">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="caf79-147">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="caf79-147">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


