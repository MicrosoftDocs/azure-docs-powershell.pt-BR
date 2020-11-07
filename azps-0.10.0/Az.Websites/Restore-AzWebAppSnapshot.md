---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: bd7c967bce709c1951cc7a61c1f8bfab9c78f28a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776066"
---
# <span data-ttu-id="0c096-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0c096-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="0c096-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c096-102">SYNOPSIS</span></span>
<span data-ttu-id="0c096-103">Restaura um instantâneo do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0c096-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="0c096-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c096-104">SYNTAX</span></span>

### <span data-ttu-id="0c096-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="0c096-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c096-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="0c096-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c096-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c096-107">DESCRIPTION</span></span>
<span data-ttu-id="0c096-108">Restaura um instantâneo do aplicativo Web para o aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0c096-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="0c096-109">Restaurar um instantâneo substitui todos os arquivos em um aplicativo Web pelos arquivos contidos no instantâneo.</span><span class="sxs-lookup"><span data-stu-id="0c096-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="0c096-110">Para restaurar as configurações também, use o parâmetro de opção RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c096-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="0c096-111">Um instantâneo de um aplicativo Web pode ser restaurado para qualquer outro aplicativo Web na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0c096-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="0c096-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c096-112">EXAMPLES</span></span>

### <span data-ttu-id="0c096-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c096-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="0c096-114">Obtém o instantâneo mais recente de um aplicativo Web chamado "ContosoApp" com um slot chamado "staging" no grupo de recursos "Default-Web-Oesteus".</span><span class="sxs-lookup"><span data-stu-id="0c096-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="0c096-115">Restaura o instantâneo para o slot "restaurar" do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0c096-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="0c096-116">OS</span><span class="sxs-lookup"><span data-stu-id="0c096-116">PARAMETERS</span></span>

### <span data-ttu-id="0c096-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c096-117">-AsJob</span></span>
<span data-ttu-id="0c096-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0c096-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c096-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c096-119">-DefaultProfile</span></span>
<span data-ttu-id="0c096-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c096-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c096-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0c096-121">-Force</span></span>
<span data-ttu-id="0c096-122">Permite que o aplicativo Web original seja substituído sem exibir um aviso.</span><span class="sxs-lookup"><span data-stu-id="0c096-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c096-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c096-123">-InputObject</span></span>
<span data-ttu-id="0c096-124">Instantâneo do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0c096-124">The Azure Web App snapshot.</span></span>
```yaml
Type: AzureWebAppSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c096-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c096-125">-Name</span></span>
<span data-ttu-id="0c096-126">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0c096-126">The name of the web app.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c096-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c096-127">-RecoverConfiguration</span></span>
<span data-ttu-id="0c096-128">Recuperar a configuração do aplicativo Web, além dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="0c096-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c096-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c096-129">-ResourceGroupName</span></span>
<span data-ttu-id="0c096-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c096-130">The name of the resource group.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c096-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="0c096-131">-Slot</span></span>
<span data-ttu-id="0c096-132">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0c096-132">The name of the web app slot.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c096-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0c096-133">-WebApp</span></span>
<span data-ttu-id="0c096-134">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="0c096-134">The web app object</span></span>
```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c096-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0c096-135">-Confirm</span></span>
<span data-ttu-id="0c096-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c096-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c096-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c096-137">-WhatIf</span></span>
<span data-ttu-id="0c096-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c096-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c096-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c096-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c096-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c096-140">CommonParameters</span></span>
<span data-ttu-id="0c096-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c096-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c096-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c096-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c096-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c096-143">INPUTS</span></span>

### <span data-ttu-id="0c096-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0c096-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="0c096-145">Microsoft. Azure. Management. WebSites. Models. site System. String Microsoft. Azure. Commands. webapps. cmdlets. BackupRestore. AzureWebAppSnapshot System. DateTime</span><span class="sxs-lookup"><span data-stu-id="0c096-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="0c096-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c096-146">OUTPUTS</span></span>

### <span data-ttu-id="0c096-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="0c096-147">System.Object</span></span>

## <span data-ttu-id="0c096-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c096-148">NOTES</span></span>

## <span data-ttu-id="0c096-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c096-149">RELATED LINKS</span></span>

