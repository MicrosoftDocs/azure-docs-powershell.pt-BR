---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a413c0b021a167252469f211b5a8e5af670f9ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774127"
---
# <span data-ttu-id="dfbc5-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="dfbc5-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="dfbc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfbc5-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbc5-103">Restaura um aplicativo Web excluído para um aplicativo Web novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="dfbc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfbc5-104">SYNTAX</span></span>

### <span data-ttu-id="dfbc5-105">FromDeletedResourceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="dfbc5-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfbc5-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="dfbc5-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfbc5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfbc5-107">DESCRIPTION</span></span>
<span data-ttu-id="dfbc5-108">O cmdlet **Restore-AzDeletedWebApp** restaura um aplicativo Web excluído.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="dfbc5-109">O aplicativo Web especificado por TargetResourceGroupName, TargetName e TargetSlot será substituído pelo conteúdo e pelas configurações do aplicativo Web excluído.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="dfbc5-110">Se os parâmetros de destino não forem especificados, eles serão automaticamente preenchidos com o grupo de recursos, o nome e o slot do aplicativo Web excluído.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="dfbc5-111">Se o aplicativo Web de destino não existir, ele será automaticamente criado no plano do serviço de aplicativo especificado por TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="dfbc5-112">O parâmetro de opção RestoreContentOnly pode ser usado para restaurar somente os arquivos do aplicativo excluído sem as configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="dfbc5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfbc5-113">EXAMPLES</span></span>

### <span data-ttu-id="dfbc5-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dfbc5-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="dfbc5-115">Restaura um aplicativo excluído denominado ContosoApp pertencente ao grupo de recursos-Web-oeste-padrão.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="dfbc5-116">Um novo aplicativo com o mesmo nome e grupo de recursos será criado no plano do serviço de aplicativo chamado ContosoPlan, e os arquivos e as configurações do aplicativo excluídos serão restaurados.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="dfbc5-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dfbc5-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="dfbc5-118">Restaura o slot de preparo de um aplicativo excluído denominado ContosoApp pertencente ao grupo de recursos-Web-Westus padrão.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="dfbc5-119">O aplicativo Web denominado ContosoRestore pertencente ao grupo de recursos padrão-Web-Eastus será substituído.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="dfbc5-120">As configurações do aplicativo Web excluído não serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="dfbc5-121">OS</span><span class="sxs-lookup"><span data-stu-id="dfbc5-121">PARAMETERS</span></span>

### <span data-ttu-id="dfbc5-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfbc5-122">-AsJob</span></span>
<span data-ttu-id="dfbc5-123">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dfbc5-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbc5-124">-DefaultProfile</span></span>
<span data-ttu-id="dfbc5-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfbc5-126">-Force</span><span class="sxs-lookup"><span data-stu-id="dfbc5-126">-Force</span></span>
<span data-ttu-id="dfbc5-127">Faça a restauração sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-127">Do the restore without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfbc5-128">-InputObject</span></span>
<span data-ttu-id="dfbc5-129">O aplicativo Web Azure excluído.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-129">The deleted Azure Web App.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-130">-Local</span><span class="sxs-lookup"><span data-stu-id="dfbc5-130">-Location</span></span>
<span data-ttu-id="dfbc5-131">O local do aplicativo Web Azure excluído.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-131">The location of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfbc5-132">-Name</span></span>
<span data-ttu-id="dfbc5-133">O nome do aplicativo Web Azure excluído.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-133">The name of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbc5-134">-ResourceGroupName</span></span>
<span data-ttu-id="dfbc5-135">O grupo de recursos do aplicativo Web Azure excluído.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-135">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-136">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="dfbc5-136">-RestoreContentOnly</span></span>
<span data-ttu-id="dfbc5-137">Restaure os arquivos do aplicativo Web, mas não restaure as configurações.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-137">Restore the web app's files, but do not restore the settings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="dfbc5-138">-Slot</span></span>
<span data-ttu-id="dfbc5-139">O slot do Azure Web App excluído.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-139">The deleted Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-140">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="dfbc5-140">-TargetAppServicePlanName</span></span>
<span data-ttu-id="dfbc5-141">O plano de serviço de aplicativo para o novo Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-141">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-142">-TargetName</span><span class="sxs-lookup"><span data-stu-id="dfbc5-142">-TargetName</span></span>
<span data-ttu-id="dfbc5-143">O nome do novo Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-143">The name of the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-144">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbc5-144">-TargetResourceGroupName</span></span>
<span data-ttu-id="dfbc5-145">O grupo de recursos que contém o novo Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-145">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-146">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="dfbc5-146">-TargetSlot</span></span>
<span data-ttu-id="dfbc5-147">O nome do novo slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-147">The name of the new Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-148">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="dfbc5-148">-UseDisasterRecovery</span></span>
<span data-ttu-id="dfbc5-149">Use para recuperar um aplicativo excluído de uma unidade de escala que está offline.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-149">Use to recover a deleted app from a scale unit that is offline.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbc5-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dfbc5-150">-Confirm</span></span>
<span data-ttu-id="dfbc5-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfbc5-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfbc5-152">-WhatIf</span></span>
<span data-ttu-id="dfbc5-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfbc5-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfbc5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbc5-155">CommonParameters</span></span>
<span data-ttu-id="dfbc5-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfbc5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbc5-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfbc5-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbc5-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfbc5-158">INPUTS</span></span>

### <span data-ttu-id="dfbc5-159">Microsoft. Azure. Commands. webapps. cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="dfbc5-159">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="dfbc5-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfbc5-160">OUTPUTS</span></span>

### <span data-ttu-id="dfbc5-161">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="dfbc5-161">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dfbc5-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfbc5-162">NOTES</span></span>

## <span data-ttu-id="dfbc5-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfbc5-163">RELATED LINKS</span></span>

[<span data-ttu-id="dfbc5-164">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="dfbc5-164">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)