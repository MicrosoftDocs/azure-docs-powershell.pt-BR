---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 536d0fe0f32231bfd732698c584e02be95d5c20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429267"
---
# <span data-ttu-id="29bda-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="29bda-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="29bda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29bda-102">SYNOPSIS</span></span>
<span data-ttu-id="29bda-103">Restaura um instantâneo do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="29bda-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29bda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29bda-104">SYNTAX</span></span>

### <span data-ttu-id="29bda-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="29bda-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29bda-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="29bda-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29bda-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29bda-107">DESCRIPTION</span></span>
<span data-ttu-id="29bda-108">Restaura um instantâneo do aplicativo Web para o aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="29bda-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="29bda-109">Restaurar um instantâneo substitui todos os arquivos em um aplicativo Web pelos arquivos contidos no instantâneo.</span><span class="sxs-lookup"><span data-stu-id="29bda-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="29bda-110">Para restaurar as configurações também, use o parâmetro de opção RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="29bda-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="29bda-111">Um instantâneo de um aplicativo Web pode ser restaurado para qualquer outro aplicativo Web na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="29bda-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="29bda-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29bda-112">EXAMPLES</span></span>

### <span data-ttu-id="29bda-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29bda-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="29bda-114">Obtém o instantâneo mais recente de um aplicativo Web chamado "ContosoApp" com um slot chamado "staging" no grupo de recursos "Default-Web-Oesteus".</span><span class="sxs-lookup"><span data-stu-id="29bda-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="29bda-115">Restaura o instantâneo para o slot "restaurar" do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="29bda-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="29bda-116">OS</span><span class="sxs-lookup"><span data-stu-id="29bda-116">PARAMETERS</span></span>

### <span data-ttu-id="29bda-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29bda-117">-AsJob</span></span>
<span data-ttu-id="29bda-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="29bda-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29bda-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bda-119">-DefaultProfile</span></span>
<span data-ttu-id="29bda-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29bda-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29bda-121">-Force</span><span class="sxs-lookup"><span data-stu-id="29bda-121">-Force</span></span>
<span data-ttu-id="29bda-122">Permite que o aplicativo Web original seja substituído sem exibir um aviso.</span><span class="sxs-lookup"><span data-stu-id="29bda-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bda-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29bda-123">-InputObject</span></span>
<span data-ttu-id="29bda-124">Instantâneo do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="29bda-124">The Azure Web App snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29bda-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="29bda-125">-Name</span></span>
<span data-ttu-id="29bda-126">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="29bda-126">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bda-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="29bda-127">-RecoverConfiguration</span></span>
<span data-ttu-id="29bda-128">Recuperar a configuração do aplicativo Web, além dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="29bda-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bda-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29bda-129">-ResourceGroupName</span></span>
<span data-ttu-id="29bda-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29bda-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bda-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="29bda-131">-Slot</span></span>
<span data-ttu-id="29bda-132">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="29bda-132">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bda-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="29bda-133">-WebApp</span></span>
<span data-ttu-id="29bda-134">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="29bda-134">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29bda-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29bda-135">-Confirm</span></span>
<span data-ttu-id="29bda-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29bda-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29bda-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29bda-137">-WhatIf</span></span>
<span data-ttu-id="29bda-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29bda-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29bda-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29bda-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29bda-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bda-140">CommonParameters</span></span>
<span data-ttu-id="29bda-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29bda-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bda-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29bda-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bda-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29bda-143">INPUTS</span></span>

### <span data-ttu-id="29bda-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="29bda-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="29bda-145">System. String</span><span class="sxs-lookup"><span data-stu-id="29bda-145">System.String</span></span>

### <span data-ttu-id="29bda-146">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="29bda-146">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="29bda-147">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="29bda-147">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="29bda-148">Microsoft. Azure. Commands. webapps. cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="29bda-148">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>
<span data-ttu-id="29bda-149">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="29bda-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="29bda-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29bda-150">OUTPUTS</span></span>

### <span data-ttu-id="29bda-151">System. void</span><span class="sxs-lookup"><span data-stu-id="29bda-151">System.Void</span></span>

## <span data-ttu-id="29bda-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29bda-152">NOTES</span></span>

## <span data-ttu-id="29bda-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29bda-153">RELATED LINKS</span></span>
