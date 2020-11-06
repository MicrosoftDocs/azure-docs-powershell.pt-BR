---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430772"
---
# <span data-ttu-id="76e6d-101">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="76e6d-101">Restore-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="76e6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="76e6d-103">Restaura um aplicativo Web excluído para um aplicativo Web novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="76e6d-103">Restores a deleted web app to a new or existing web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76e6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76e6d-104">SYNTAX</span></span>

### <span data-ttu-id="76e6d-105">FromDeletedResourceName</span><span class="sxs-lookup"><span data-stu-id="76e6d-105">FromDeletedResourceName</span></span>
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76e6d-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="76e6d-106">FromDeletedApp</span></span>
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## <span data-ttu-id="76e6d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76e6d-107">DESCRIPTION</span></span>
<span data-ttu-id="76e6d-108">O cmdlet **Restore-AzureRmDeletedWebApp** restaura um aplicativo Web excluído.</span><span class="sxs-lookup"><span data-stu-id="76e6d-108">The **Restore-AzureRmDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="76e6d-109">O aplicativo Web especificado por TargetResourceGroupName, TargetName e TargetSlot será substituído pelo conteúdo e pelas configurações do aplicativo Web excluído.</span><span class="sxs-lookup"><span data-stu-id="76e6d-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="76e6d-110">Se os parâmetros de destino não forem especificados, eles serão automaticamente preenchidos com o grupo de recursos, o nome e o slot do aplicativo Web excluído.</span><span class="sxs-lookup"><span data-stu-id="76e6d-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="76e6d-111">Se o aplicativo Web de destino não existir, ele será automaticamente criado no plano do serviço de aplicativo especificado por TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="76e6d-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="76e6d-112">O parâmetro de opção RestoreContentOnly pode ser usado para restaurar somente os arquivos do aplicativo excluído sem as configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="76e6d-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="76e6d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76e6d-113">EXAMPLES</span></span>

### <span data-ttu-id="76e6d-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76e6d-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="76e6d-115">Restaura um aplicativo excluído denominado ContosoApp pertencente ao grupo de recursos-Web-oeste-padrão.</span><span class="sxs-lookup"><span data-stu-id="76e6d-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="76e6d-116">Um novo aplicativo com o mesmo nome e grupo de recursos será criado no plano do serviço de aplicativo chamado ContosoPlan, e os arquivos e as configurações do aplicativo excluídos serão restaurados.</span><span class="sxs-lookup"><span data-stu-id="76e6d-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="76e6d-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="76e6d-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="76e6d-118">Restaura o slot de preparo de um aplicativo excluído denominado ContosoApp pertencente ao grupo de recursos-Web-Westus padrão.</span><span class="sxs-lookup"><span data-stu-id="76e6d-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="76e6d-119">O aplicativo Web denominado ContosoRestore pertencente ao grupo de recursos padrão-Web-Eastus será substituído.</span><span class="sxs-lookup"><span data-stu-id="76e6d-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="76e6d-120">As configurações do aplicativo Web excluído não serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="76e6d-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="76e6d-121">OS</span><span class="sxs-lookup"><span data-stu-id="76e6d-121">PARAMETERS</span></span>

### <span data-ttu-id="76e6d-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76e6d-122">-AsJob</span></span>
<span data-ttu-id="76e6d-123">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="76e6d-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e6d-124">-DefaultProfile</span></span>
<span data-ttu-id="76e6d-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76e6d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="76e6d-126">-Force</span></span>
<span data-ttu-id="76e6d-127">Faça a restauração sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="76e6d-127">Do the restore without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76e6d-128">-InputObject</span></span>
<span data-ttu-id="76e6d-129">O aplicativo Web Azure excluído.</span><span class="sxs-lookup"><span data-stu-id="76e6d-129">The deleted Azure Web App.</span></span>

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="76e6d-130">-Name</span></span>
<span data-ttu-id="76e6d-131">O nome do aplicativo Web Azure excluído.</span><span class="sxs-lookup"><span data-stu-id="76e6d-131">The name of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76e6d-132">-ResourceGroupName</span></span>
<span data-ttu-id="76e6d-133">O grupo de recursos do aplicativo Web Azure excluído.</span><span class="sxs-lookup"><span data-stu-id="76e6d-133">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="76e6d-134">-RestoreContentOnly</span></span>
<span data-ttu-id="76e6d-135">Restaure os arquivos do aplicativo Web, mas não restaure as configurações.</span><span class="sxs-lookup"><span data-stu-id="76e6d-135">Restore the web app's files, but do not restore the settings.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="76e6d-136">-Slot</span></span>
<span data-ttu-id="76e6d-137">O slot do Azure Web App excluído.</span><span class="sxs-lookup"><span data-stu-id="76e6d-137">The deleted Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="76e6d-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="76e6d-139">O plano de serviço de aplicativo para o novo Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="76e6d-139">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="76e6d-140">-TargetName</span></span>
<span data-ttu-id="76e6d-141">O nome do novo Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="76e6d-141">The name of the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76e6d-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="76e6d-143">O grupo de recursos que contém o novo Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="76e6d-143">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="76e6d-144">-TargetSlot</span></span>
<span data-ttu-id="76e6d-145">O nome do novo slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="76e6d-145">The name of the new Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e6d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e6d-146">CommonParameters</span></span>
<span data-ttu-id="76e6d-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76e6d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="76e6d-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76e6d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e6d-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76e6d-149">INPUTS</span></span>

### <span data-ttu-id="76e6d-150">Microsoft. Azure. Commands. webapps. cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="76e6d-150">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="76e6d-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76e6d-151">OUTPUTS</span></span>

### <span data-ttu-id="76e6d-152">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="76e6d-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="76e6d-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76e6d-153">NOTES</span></span>

## <span data-ttu-id="76e6d-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76e6d-154">RELATED LINKS</span></span>

[<span data-ttu-id="76e6d-155">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="76e6d-155">Get-AzureRmDeletedWebApp</span></span>](./Get-AzureRmDeletedWebApp.md)
