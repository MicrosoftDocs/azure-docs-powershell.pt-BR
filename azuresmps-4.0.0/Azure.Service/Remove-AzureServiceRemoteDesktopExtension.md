---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946112"
---
# <span data-ttu-id="23000-101">Remove-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="23000-101">Remove-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="23000-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23000-102">SYNOPSIS</span></span>
<span data-ttu-id="23000-103">Remove a extensão da área de trabalho remota do serviço de nuvem aplicada a todas as funções ou funções nomeadas em um slot de implantação especificado.</span><span class="sxs-lookup"><span data-stu-id="23000-103">Removes the cloud service remote desktop extension applied on all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="23000-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23000-104">SYNTAX</span></span>

### <span data-ttu-id="23000-105">RemoveByRoles (padrão)</span><span class="sxs-lookup"><span data-stu-id="23000-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="23000-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="23000-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="23000-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23000-107">DESCRIPTION</span></span>
<span data-ttu-id="23000-108">O cmdlet **Remove-AzureServiceRemoteDesktopExtension** remove a extensão da área de trabalho remota do serviço de nuvem aplicada a todas as funções ou funções nomeadas em um determinado slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="23000-108">The **Remove-AzureServiceRemoteDesktopExtension** cmdlet removes the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="23000-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23000-109">EXAMPLES</span></span>

### <span data-ttu-id="23000-110">Exemplo 1: remover a extensão da área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="23000-110">Example 1: Remove the remote desktop extension</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="23000-111">Esse comando Remove a extensão da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="23000-111">This command removes the remote desktop extension.</span></span>

### <span data-ttu-id="23000-112">Exemplo 2: remover a extensão da área de trabalho remota de uma função especificada</span><span class="sxs-lookup"><span data-stu-id="23000-112">Example 2: Remove the remote desktop extension from a specified role</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

<span data-ttu-id="23000-113">Este comando Remove a extensão da área de trabalho remota de uma função especificada.</span><span class="sxs-lookup"><span data-stu-id="23000-113">This command removes the remote desktop extension from a specified role.</span></span>

## <span data-ttu-id="23000-114">OS</span><span class="sxs-lookup"><span data-stu-id="23000-114">PARAMETERS</span></span>

### <span data-ttu-id="23000-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="23000-115">-InformationAction</span></span>
<span data-ttu-id="23000-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="23000-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23000-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="23000-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23000-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="23000-118">Continue</span></span>
- <span data-ttu-id="23000-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="23000-119">Ignore</span></span>
- <span data-ttu-id="23000-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="23000-120">Inquire</span></span>
- <span data-ttu-id="23000-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23000-121">SilentlyContinue</span></span>
- <span data-ttu-id="23000-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="23000-122">Stop</span></span>
- <span data-ttu-id="23000-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="23000-123">Suspend</span></span>

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

### <span data-ttu-id="23000-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23000-124">-InformationVariable</span></span>
<span data-ttu-id="23000-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="23000-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="23000-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="23000-126">-Profile</span></span>
<span data-ttu-id="23000-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="23000-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23000-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="23000-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23000-129">-Função</span><span class="sxs-lookup"><span data-stu-id="23000-129">-Role</span></span>
<span data-ttu-id="23000-130">Especifica uma matriz opcional de funções para especificar a configuração da área de trabalho remota para.</span><span class="sxs-lookup"><span data-stu-id="23000-130">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="23000-131">Se não especificado, a configuração da área de trabalho remota será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="23000-131">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="23000-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="23000-132">-ServiceName</span></span>
<span data-ttu-id="23000-133">Especifica o nome do serviço do Azure da implantação.</span><span class="sxs-lookup"><span data-stu-id="23000-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="23000-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="23000-134">-Slot</span></span>
<span data-ttu-id="23000-135">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="23000-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="23000-136">Os valores com suporte são "produção" ou "preparação".</span><span class="sxs-lookup"><span data-stu-id="23000-136">Supported values are "Production" or "Staging".</span></span>

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

### <span data-ttu-id="23000-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="23000-137">-UninstallConfiguration</span></span>
<span data-ttu-id="23000-138">Especifica que esse cmdlet desinstale todas as configurações de RDP do serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="23000-138">Specifies that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="23000-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23000-139">CommonParameters</span></span>
<span data-ttu-id="23000-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23000-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23000-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23000-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23000-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23000-142">INPUTS</span></span>

## <span data-ttu-id="23000-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23000-143">OUTPUTS</span></span>

## <span data-ttu-id="23000-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23000-144">NOTES</span></span>

## <span data-ttu-id="23000-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23000-145">RELATED LINKS</span></span>

[<span data-ttu-id="23000-146">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="23000-146">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


