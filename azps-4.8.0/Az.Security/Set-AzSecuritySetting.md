---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110874"
---
# <span data-ttu-id="1c220-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="1c220-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="1c220-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c220-102">SYNOPSIS</span></span>
<span data-ttu-id="1c220-103">Atualizar uma configuração de segurança na central de segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="1c220-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="1c220-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c220-104">SYNTAX</span></span>

### <span data-ttu-id="1c220-105">GeneralScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="1c220-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c220-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="1c220-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c220-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1c220-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c220-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c220-108">DESCRIPTION</span></span>
<span data-ttu-id="1c220-109">O cmdlet Set-AzSecuritySetting atualiza uma configuração de segurança específica na central de segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c220-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="1c220-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c220-110">EXAMPLES</span></span>

### <span data-ttu-id="1c220-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c220-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="1c220-112">Atualiza uma configuração de exportação de dados do MCAS</span><span class="sxs-lookup"><span data-stu-id="1c220-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="1c220-113">OS</span><span class="sxs-lookup"><span data-stu-id="1c220-113">PARAMETERS</span></span>

### <span data-ttu-id="1c220-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c220-114">-DefaultProfile</span></span>
<span data-ttu-id="1c220-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c220-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c220-116">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="1c220-116">-Enabled</span></span>
<span data-ttu-id="1c220-117">Habilita a configuração.</span><span class="sxs-lookup"><span data-stu-id="1c220-117">Enables the setting.</span></span>

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

### <span data-ttu-id="1c220-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c220-118">-InputObject</span></span>
<span data-ttu-id="1c220-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="1c220-119">Input Object.</span></span>

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

### <span data-ttu-id="1c220-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="1c220-120">-SettingKind</span></span>
<span data-ttu-id="1c220-121">Configuração de tipo.</span><span class="sxs-lookup"><span data-stu-id="1c220-121">Setting kind.</span></span> <span data-ttu-id="1c220-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="1c220-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="1c220-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="1c220-123">-SettingName</span></span>
<span data-ttu-id="1c220-124">Nome da configuração.</span><span class="sxs-lookup"><span data-stu-id="1c220-124">Setting name.</span></span> <span data-ttu-id="1c220-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="1c220-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="1c220-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c220-126">-Confirm</span></span>
<span data-ttu-id="1c220-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c220-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c220-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c220-128">-WhatIf</span></span>
<span data-ttu-id="1c220-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c220-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c220-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c220-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c220-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c220-131">CommonParameters</span></span>
<span data-ttu-id="1c220-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c220-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c220-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c220-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c220-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c220-134">INPUTS</span></span>

### <span data-ttu-id="1c220-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1c220-135">System.String</span></span>
### <span data-ttu-id="1c220-136">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="1c220-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="1c220-137">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="1c220-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="1c220-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c220-138">System.Boolean</span></span>

## <span data-ttu-id="1c220-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c220-139">OUTPUTS</span></span>

### <span data-ttu-id="1c220-140">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="1c220-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="1c220-141">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="1c220-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="1c220-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c220-142">NOTES</span></span>

## <span data-ttu-id="1c220-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c220-143">RELATED LINKS</span></span>
