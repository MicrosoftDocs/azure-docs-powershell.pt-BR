---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260116"
---
# <span data-ttu-id="583ce-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="583ce-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="583ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="583ce-102">SYNOPSIS</span></span>
<span data-ttu-id="583ce-103">Atualizar uma configuração de segurança na central de segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="583ce-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="583ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="583ce-104">SYNTAX</span></span>

### <span data-ttu-id="583ce-105">GeneralScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="583ce-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="583ce-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="583ce-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="583ce-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="583ce-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="583ce-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="583ce-108">DESCRIPTION</span></span>
<span data-ttu-id="583ce-109">O cmdlet Set-AzSecuritySetting atualiza uma configuração de segurança específica na central de segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="583ce-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="583ce-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="583ce-110">EXAMPLES</span></span>

### <span data-ttu-id="583ce-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="583ce-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="583ce-112">Atualiza uma configuração de exportação de dados do MCAS</span><span class="sxs-lookup"><span data-stu-id="583ce-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="583ce-113">OS</span><span class="sxs-lookup"><span data-stu-id="583ce-113">PARAMETERS</span></span>

### <span data-ttu-id="583ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="583ce-114">-DefaultProfile</span></span>
<span data-ttu-id="583ce-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="583ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="583ce-116">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="583ce-116">-Enabled</span></span>
<span data-ttu-id="583ce-117">Habilita a configuração.</span><span class="sxs-lookup"><span data-stu-id="583ce-117">Enables the setting.</span></span>

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

### <span data-ttu-id="583ce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="583ce-118">-InputObject</span></span>
<span data-ttu-id="583ce-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="583ce-119">Input Object.</span></span>

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

### <span data-ttu-id="583ce-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="583ce-120">-SettingKind</span></span>
<span data-ttu-id="583ce-121">Configuração de tipo.</span><span class="sxs-lookup"><span data-stu-id="583ce-121">Setting kind.</span></span> <span data-ttu-id="583ce-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="583ce-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="583ce-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="583ce-123">-SettingName</span></span>
<span data-ttu-id="583ce-124">Nome da configuração.</span><span class="sxs-lookup"><span data-stu-id="583ce-124">Setting name.</span></span> <span data-ttu-id="583ce-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="583ce-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="583ce-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="583ce-126">-Confirm</span></span>
<span data-ttu-id="583ce-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="583ce-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="583ce-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="583ce-128">-WhatIf</span></span>
<span data-ttu-id="583ce-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="583ce-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="583ce-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="583ce-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="583ce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583ce-131">CommonParameters</span></span>
<span data-ttu-id="583ce-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="583ce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583ce-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="583ce-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583ce-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="583ce-134">INPUTS</span></span>

### <span data-ttu-id="583ce-135">System. String</span><span class="sxs-lookup"><span data-stu-id="583ce-135">System.String</span></span>
### <span data-ttu-id="583ce-136">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="583ce-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="583ce-137">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="583ce-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="583ce-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="583ce-138">System.Boolean</span></span>

## <span data-ttu-id="583ce-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="583ce-139">OUTPUTS</span></span>

### <span data-ttu-id="583ce-140">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="583ce-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="583ce-141">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="583ce-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="583ce-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="583ce-142">NOTES</span></span>

## <span data-ttu-id="583ce-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="583ce-143">RELATED LINKS</span></span>
