---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118845"
---
# <span data-ttu-id="53e40-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="53e40-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="53e40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53e40-102">SYNOPSIS</span></span>
<span data-ttu-id="53e40-103">Remove uma encadernação SSL de um certificado carregado.</span><span class="sxs-lookup"><span data-stu-id="53e40-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="53e40-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53e40-104">SYNTAX</span></span>

### <span data-ttu-id="53e40-105">S1</span><span class="sxs-lookup"><span data-stu-id="53e40-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53e40-106">S2</span><span class="sxs-lookup"><span data-stu-id="53e40-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53e40-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="53e40-107">DESCRIPTION</span></span>
<span data-ttu-id="53e40-108">O cmdlet **Remove-AzWebAppSSLBinding** remove uma encadernação SSL (Secure Sockets Layer) de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="53e40-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="53e40-109">As associações SSL são usadas para associar um Web App a um certificado.</span><span class="sxs-lookup"><span data-stu-id="53e40-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="53e40-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="53e40-110">EXAMPLES</span></span>

### <span data-ttu-id="53e40-111">Exemplo 1: Remover uma associação SSL para um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="53e40-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="53e40-112">Esse comando remove a associação SSL do aplicativo Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="53e40-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="53e40-113">Como o *parâmetro DeleteCertificate* não está incluído, o certificado será excluído se ele não tiver mais nenhuma associação SSL.</span><span class="sxs-lookup"><span data-stu-id="53e40-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="53e40-114">Exemplo 2: Remover uma associação SSL sem remover o certificado</span><span class="sxs-lookup"><span data-stu-id="53e40-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="53e40-115">Semelhante ao Exemplo 1, esse comando também remove a associação SSL do Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="53e40-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="53e40-116">Nesse caso, no entanto, o parâmetro *DeleteCertificate* é incluído e o valor do parâmetro é definido como $False.</span><span class="sxs-lookup"><span data-stu-id="53e40-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="53e40-117">Isso significa que o certificado não será excluído independentemente de ter alguma vinculação SSL ou não.</span><span class="sxs-lookup"><span data-stu-id="53e40-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="53e40-118">Exemplo 3: Usar uma referência de objeto para remover uma associação SSL</span><span class="sxs-lookup"><span data-stu-id="53e40-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="53e40-119">Este exemplo usa uma referência de objeto ao site do Web App para remover a associação SSL de um Web App.</span><span class="sxs-lookup"><span data-stu-id="53e40-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="53e40-120">O primeiro comando usa o cmdlet Get-AzWebApp para criar uma referência de objeto ao Web App chamada ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="53e40-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="53e40-121">Essa referência de objeto é armazenada em uma variável chamada $WebApp.</span><span class="sxs-lookup"><span data-stu-id="53e40-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="53e40-122">O segundo comando usa a referência de objeto e o cmdlet **Remove-AzWebAppSSLBinding** para remover a associação SSL.</span><span class="sxs-lookup"><span data-stu-id="53e40-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="53e40-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53e40-123">PARAMETERS</span></span>

### <span data-ttu-id="53e40-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53e40-124">-DefaultProfile</span></span>
<span data-ttu-id="53e40-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="53e40-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53e40-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="53e40-126">-DeleteCertificate</span></span>
<span data-ttu-id="53e40-127">Especifica a ação a ser realizada se a encadernação SSL que está sendo removida for a única associação usada pelo certificado.</span><span class="sxs-lookup"><span data-stu-id="53e40-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="53e40-128">Se *DeleteCertificate* estiver definido como $False, o certificado não será excluído quando a associação for excluída.</span><span class="sxs-lookup"><span data-stu-id="53e40-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="53e40-129">Se *DeleteCertificate* estiver definido como $True ou não estiver incluído no comando, o certificado será excluído juntamente com a associação SSL.</span><span class="sxs-lookup"><span data-stu-id="53e40-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="53e40-130">O certificado só será excluído se a associação SSL for removida for a única vinculação usada pelo certificado.</span><span class="sxs-lookup"><span data-stu-id="53e40-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="53e40-131">Se o certificado tiver mais de uma vinculação, o certificado não será removido independentemente do valor do parâmetro *DeleteCertificate.*</span><span class="sxs-lookup"><span data-stu-id="53e40-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-132">-Forçar</span><span class="sxs-lookup"><span data-stu-id="53e40-132">-Force</span></span>
<span data-ttu-id="53e40-133">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="53e40-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="53e40-134">-Name</span></span>
<span data-ttu-id="53e40-135">Especifica o nome do Web App.</span><span class="sxs-lookup"><span data-stu-id="53e40-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53e40-136">-ResourceGroupName</span></span>
<span data-ttu-id="53e40-137">Especifica o nome do grupo de recursos ao que o certificado foi atribuído.</span><span class="sxs-lookup"><span data-stu-id="53e40-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="53e40-138">Você não pode usar *o parâmetro ResourceGroupName* e o parâmetro *WebApp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="53e40-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="53e40-139">-Slot</span></span>
<span data-ttu-id="53e40-140">Especifica o slot de implantação do Web App.</span><span class="sxs-lookup"><span data-stu-id="53e40-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="53e40-141">Para obter um slot de implantação, use Get-AzWebAppSlot cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53e40-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="53e40-142">-WebApp</span></span>
<span data-ttu-id="53e40-143">Especifica um Web App.</span><span class="sxs-lookup"><span data-stu-id="53e40-143">Specifies a Web App.</span></span>
<span data-ttu-id="53e40-144">Para obter um Web App, use o Get-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53e40-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="53e40-145">Você não pode usar o parâmetro *WebApp* no mesmo comando que o parâmetro *ResourceGroupName* e/ou *WebAppName.*</span><span class="sxs-lookup"><span data-stu-id="53e40-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="53e40-146">-WebAppName</span></span>
<span data-ttu-id="53e40-147">Especifica o nome do Web App.</span><span class="sxs-lookup"><span data-stu-id="53e40-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="53e40-148">Você não pode usar o parâmetro *WebAppName* e o parâmetro *WebApp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="53e40-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-149">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="53e40-149">-Confirm</span></span>
<span data-ttu-id="53e40-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53e40-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53e40-151">-WhatIf</span></span>
<span data-ttu-id="53e40-152">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="53e40-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53e40-153">O cmdlet não é executado. Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="53e40-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53e40-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53e40-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e40-155">CommonParameters</span></span>
<span data-ttu-id="53e40-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53e40-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e40-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53e40-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e40-158">Entradas</span><span class="sxs-lookup"><span data-stu-id="53e40-158">INPUTS</span></span>

### <span data-ttu-id="53e40-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="53e40-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="53e40-160">Saídas</span><span class="sxs-lookup"><span data-stu-id="53e40-160">OUTPUTS</span></span>

### <span data-ttu-id="53e40-161">System.Void</span><span class="sxs-lookup"><span data-stu-id="53e40-161">System.Void</span></span>

## <span data-ttu-id="53e40-162">Notas</span><span class="sxs-lookup"><span data-stu-id="53e40-162">NOTES</span></span>

## <span data-ttu-id="53e40-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53e40-163">RELATED LINKS</span></span>

[<span data-ttu-id="53e40-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="53e40-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="53e40-165">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="53e40-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="53e40-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53e40-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="53e40-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="53e40-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


