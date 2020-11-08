---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125182"
---
# <span data-ttu-id="937c8-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="937c8-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="937c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="937c8-102">SYNOPSIS</span></span>
<span data-ttu-id="937c8-103">Restaura um instantâneo do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="937c8-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="937c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="937c8-104">SYNTAX</span></span>

### <span data-ttu-id="937c8-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="937c8-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="937c8-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="937c8-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="937c8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="937c8-107">DESCRIPTION</span></span>
<span data-ttu-id="937c8-108">Restaura um instantâneo do aplicativo Web para o aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="937c8-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="937c8-109">Restaurar um instantâneo substitui todos os arquivos em um aplicativo Web pelos arquivos contidos no instantâneo.</span><span class="sxs-lookup"><span data-stu-id="937c8-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="937c8-110">Para restaurar as configurações também, use o parâmetro de opção RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="937c8-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="937c8-111">Um instantâneo de um aplicativo Web pode ser restaurado para qualquer outro aplicativo Web na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="937c8-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="937c8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="937c8-112">EXAMPLES</span></span>

### <span data-ttu-id="937c8-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="937c8-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="937c8-114">Obtém o instantâneo mais recente de um aplicativo Web chamado "ContosoApp" com um slot chamado "staging" no grupo de recursos "Default-Web-Oesteus".</span><span class="sxs-lookup"><span data-stu-id="937c8-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="937c8-115">Restaura o instantâneo para o slot "restaurar" do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="937c8-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="937c8-116">OS</span><span class="sxs-lookup"><span data-stu-id="937c8-116">PARAMETERS</span></span>

### <span data-ttu-id="937c8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="937c8-117">-AsJob</span></span>
<span data-ttu-id="937c8-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="937c8-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="937c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937c8-119">-DefaultProfile</span></span>
<span data-ttu-id="937c8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="937c8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="937c8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="937c8-121">-Force</span></span>
<span data-ttu-id="937c8-122">Permite que o aplicativo Web original seja substituído sem exibir um aviso.</span><span class="sxs-lookup"><span data-stu-id="937c8-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="937c8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="937c8-123">-InputObject</span></span>
<span data-ttu-id="937c8-124">Instantâneo do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="937c8-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="937c8-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="937c8-125">-Name</span></span>
<span data-ttu-id="937c8-126">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="937c8-126">The name of the web app.</span></span>

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

### <span data-ttu-id="937c8-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="937c8-127">-RecoverConfiguration</span></span>
<span data-ttu-id="937c8-128">Recuperar a configuração do aplicativo Web, além dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="937c8-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="937c8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="937c8-129">-ResourceGroupName</span></span>
<span data-ttu-id="937c8-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="937c8-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="937c8-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="937c8-131">-Slot</span></span>
<span data-ttu-id="937c8-132">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="937c8-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="937c8-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="937c8-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="937c8-134">Use para recuperar um instantâneo de uma unidade de escala que está offline.</span><span class="sxs-lookup"><span data-stu-id="937c8-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="937c8-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="937c8-135">-WebApp</span></span>
<span data-ttu-id="937c8-136">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="937c8-136">The web app object</span></span>

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

### <span data-ttu-id="937c8-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="937c8-137">-Confirm</span></span>
<span data-ttu-id="937c8-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="937c8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="937c8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="937c8-139">-WhatIf</span></span>
<span data-ttu-id="937c8-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="937c8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="937c8-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="937c8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="937c8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937c8-142">CommonParameters</span></span>
<span data-ttu-id="937c8-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="937c8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937c8-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="937c8-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937c8-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="937c8-145">INPUTS</span></span>

### <span data-ttu-id="937c8-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="937c8-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="937c8-147">System. String</span><span class="sxs-lookup"><span data-stu-id="937c8-147">System.String</span></span>

### <span data-ttu-id="937c8-148">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="937c8-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="937c8-149">Microsoft. Azure. Commands. webapps. cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="937c8-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="937c8-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="937c8-150">OUTPUTS</span></span>

### <span data-ttu-id="937c8-151">System. void</span><span class="sxs-lookup"><span data-stu-id="937c8-151">System.Void</span></span>

## <span data-ttu-id="937c8-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="937c8-152">NOTES</span></span>

## <span data-ttu-id="937c8-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="937c8-153">RELATED LINKS</span></span>
