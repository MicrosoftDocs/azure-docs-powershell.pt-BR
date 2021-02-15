---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112606"
---
# <span data-ttu-id="961d8-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="961d8-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="961d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="961d8-102">SYNOPSIS</span></span>
<span data-ttu-id="961d8-103">Atualizar uma configuração de segurança no Centro de Segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="961d8-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="961d8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="961d8-104">SYNTAX</span></span>

### <span data-ttu-id="961d8-105">GeneralScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="961d8-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="961d8-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="961d8-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="961d8-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="961d8-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="961d8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="961d8-108">DESCRIPTION</span></span>
<span data-ttu-id="961d8-109">O Set-AzSecuritySetting cmdlet atualiza uma configuração de segurança específica no Centro de Segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="961d8-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="961d8-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="961d8-110">EXAMPLES</span></span>

### <span data-ttu-id="961d8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="961d8-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="961d8-112">Atualiza uma configuração de exportação de dados MCAS</span><span class="sxs-lookup"><span data-stu-id="961d8-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="961d8-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="961d8-113">PARAMETERS</span></span>

### <span data-ttu-id="961d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="961d8-114">-DefaultProfile</span></span>
<span data-ttu-id="961d8-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="961d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961d8-116">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="961d8-116">-Enabled</span></span>
<span data-ttu-id="961d8-117">Habilita a configuração.</span><span class="sxs-lookup"><span data-stu-id="961d8-117">Enables the setting.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961d8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="961d8-118">-InputObject</span></span>
<span data-ttu-id="961d8-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="961d8-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="961d8-120">-SettingEar</span><span class="sxs-lookup"><span data-stu-id="961d8-120">-SettingKind</span></span>
<span data-ttu-id="961d8-121">Tipo de configuração.</span><span class="sxs-lookup"><span data-stu-id="961d8-121">Setting kind.</span></span> <span data-ttu-id="961d8-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="961d8-122">(DataExportSettings)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961d8-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="961d8-123">-SettingName</span></span>
<span data-ttu-id="961d8-124">Nome da configuração.</span><span class="sxs-lookup"><span data-stu-id="961d8-124">Setting name.</span></span> <span data-ttu-id="961d8-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="961d8-125">(MCAS/WDATP)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961d8-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="961d8-126">-Confirm</span></span>
<span data-ttu-id="961d8-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="961d8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="961d8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="961d8-128">-WhatIf</span></span>
<span data-ttu-id="961d8-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="961d8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="961d8-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="961d8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="961d8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="961d8-131">CommonParameters</span></span>
<span data-ttu-id="961d8-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="961d8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="961d8-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="961d8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="961d8-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="961d8-134">INPUTS</span></span>

### <span data-ttu-id="961d8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="961d8-135">System.String</span></span>
### <span data-ttu-id="961d8-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="961d8-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="961d8-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="961d8-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="961d8-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="961d8-138">System.Boolean</span></span>

## <span data-ttu-id="961d8-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="961d8-139">OUTPUTS</span></span>

### <span data-ttu-id="961d8-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="961d8-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="961d8-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="961d8-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="961d8-142">Notas</span><span class="sxs-lookup"><span data-stu-id="961d8-142">NOTES</span></span>

## <span data-ttu-id="961d8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="961d8-143">RELATED LINKS</span></span>
