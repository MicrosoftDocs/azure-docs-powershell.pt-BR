---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 81807c92b336bd171d0890f5b3e948ec11313023
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891910"
---
# <span data-ttu-id="cc2f6-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="cc2f6-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="cc2f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="cc2f6-103">Restaura um aplicativo Web excluído para um aplicativo Web novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="cc2f6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cc2f6-104">SYNTAX</span></span>

### <span data-ttu-id="cc2f6-105">FromDeletedResourceName (Default)</span><span class="sxs-lookup"><span data-stu-id="cc2f6-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc2f6-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="cc2f6-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc2f6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cc2f6-107">DESCRIPTION</span></span>
<span data-ttu-id="cc2f6-108">O cmdlet **Restore-AzDeletedWebApp** restaura um aplicativo Web excluído.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="cc2f6-109">O aplicativo Web especificado por TargetResourceGroupName, TargetName e TargetSlot será substituído com o conteúdo e as configurações do aplicativo Web excluído.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="cc2f6-110">Se os parâmetros de destino não são especificados, eles serão preenchidos automaticamente com o grupo de recursos, o nome e o slot do aplicativo Web excluído.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="cc2f6-111">Se o aplicativo Web de destino não existir, ele será criado automaticamente no plano de serviço de aplicativo especificado por TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="cc2f6-112">O parâmetro de opção RestoreContentOnly pode ser usado para restaurar apenas os arquivos do aplicativo excluído sem as configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="cc2f6-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc2f6-113">EXAMPLES</span></span>

### <span data-ttu-id="cc2f6-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc2f6-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="cc2f6-115">Restaura um aplicativo excluído chamado ContosoApp pertencente ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="cc2f6-116">Um novo aplicativo com o mesmo nome e grupo de recursos será criado no Plano de Serviço de Aplicativo chamado ContosoPlan, e os arquivos e configurações do aplicativo excluído serão restaurados para ele.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="cc2f6-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cc2f6-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="cc2f6-118">Restaura o slot de preparação de um aplicativo excluído chamado ContosoApp pertencente ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="cc2f6-119">O aplicativo Web chamado ContosoRestore pertencente ao grupo de recursos Default-Web-EastUS será substituído.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="cc2f6-120">As configurações do aplicativo Web excluídas não serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="cc2f6-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="cc2f6-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="cc2f6-122">Caso haja 2 aplicativos excluídos com o mesmo nome(ContosoApp), então obteremos detalhes dos sites e restauraremos o aplicativo chamado ContosoRestore com o aplicativo de nossa escolha chamando restauração com ID.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="cc2f6-123">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="cc2f6-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="cc2f6-124">Caso haja 2 aplicativos excluídos com o mesmo nome(ContosoApp), obteremos detalhes dos sites e restauraremos o aplicativo chamado ContosoRestore com o aplicativo de nossa escolha chamando restauração com detalhes inputObject(Deletedsite)</span><span class="sxs-lookup"><span data-stu-id="cc2f6-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="cc2f6-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cc2f6-125">PARAMETERS</span></span>

### <span data-ttu-id="cc2f6-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc2f6-126">-AsJob</span></span>
<span data-ttu-id="cc2f6-127">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cc2f6-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc2f6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc2f6-128">-DefaultProfile</span></span>
<span data-ttu-id="cc2f6-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc2f6-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="cc2f6-130">-DeletedId</span></span>
<span data-ttu-id="cc2f6-131">A ID do Azure Web App excluído.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-131">The Id of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="cc2f6-132">-Force</span><span class="sxs-lookup"><span data-stu-id="cc2f6-132">-Force</span></span>
<span data-ttu-id="cc2f6-133">Faça a restauração sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cc2f6-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc2f6-134">-InputObject</span></span>
<span data-ttu-id="cc2f6-135">O Aplicativo Web do Azure excluído.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-135">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="cc2f6-136">-Location</span><span class="sxs-lookup"><span data-stu-id="cc2f6-136">-Location</span></span>
<span data-ttu-id="cc2f6-137">O local do Azure Web App excluído.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-137">The location of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="cc2f6-138">-Name</span><span class="sxs-lookup"><span data-stu-id="cc2f6-138">-Name</span></span>
<span data-ttu-id="cc2f6-139">O nome do Azure Web App excluído.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-139">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="cc2f6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc2f6-140">-ResourceGroupName</span></span>
<span data-ttu-id="cc2f6-141">O grupo de recursos do Azure Web App excluído.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-141">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="cc2f6-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="cc2f6-142">-RestoreContentOnly</span></span>
<span data-ttu-id="cc2f6-143">Restaure os arquivos do aplicativo Web, mas não restaure as configurações.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="cc2f6-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="cc2f6-144">-Slot</span></span>
<span data-ttu-id="cc2f6-145">O slot excluído do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-145">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="cc2f6-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="cc2f6-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="cc2f6-147">O Plano de Serviço de Aplicativo para o novo Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="cc2f6-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="cc2f6-148">-TargetName</span></span>
<span data-ttu-id="cc2f6-149">O nome do novo Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="cc2f6-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc2f6-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="cc2f6-151">O grupo de recursos que contém o novo Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="cc2f6-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="cc2f6-152">-TargetSlot</span></span>
<span data-ttu-id="cc2f6-153">O nome do novo slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="cc2f6-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="cc2f6-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="cc2f6-155">Use para recuperar um aplicativo excluído de uma unidade de escala que está offline.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="cc2f6-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc2f6-156">-Confirm</span></span>
<span data-ttu-id="cc2f6-157">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc2f6-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc2f6-158">-WhatIf</span></span>
<span data-ttu-id="cc2f6-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc2f6-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc2f6-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc2f6-161">CommonParameters</span></span>
<span data-ttu-id="cc2f6-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc2f6-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc2f6-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc2f6-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc2f6-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc2f6-164">INPUTS</span></span>

### <span data-ttu-id="cc2f6-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="cc2f6-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="cc2f6-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cc2f6-166">OUTPUTS</span></span>

### <span data-ttu-id="cc2f6-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="cc2f6-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cc2f6-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="cc2f6-168">NOTES</span></span>

## <span data-ttu-id="cc2f6-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc2f6-169">RELATED LINKS</span></span>

[<span data-ttu-id="cc2f6-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="cc2f6-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)