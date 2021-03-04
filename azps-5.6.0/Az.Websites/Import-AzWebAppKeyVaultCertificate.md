---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: d92aa19573a238d7f54a21f7888bbd93ac07107b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892579"
---
# <span data-ttu-id="36718-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="36718-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="36718-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36718-102">SYNOPSIS</span></span>
<span data-ttu-id="36718-103">Importe um certificado SSL para um aplicativo Web do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="36718-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="36718-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="36718-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36718-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="36718-105">DESCRIPTION</span></span>
<span data-ttu-id="36718-106">O cmdlet **Import-AzWebAppKeyVaultCertificate** importa um certificado SSL para um aplicativo Web do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="36718-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="36718-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36718-107">EXAMPLES</span></span>

### <span data-ttu-id="36718-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="36718-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="36718-109">Este comando importa um certificado SSL para um aplicativo Web do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="36718-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="36718-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="36718-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="36718-111">Este comando Importar um certificado SSL para um aplicativo Web do Key Vault usando a ID do recurso (geralmente se o Cofre de Chaves estiver em outra assinatura).</span><span class="sxs-lookup"><span data-stu-id="36718-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="36718-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="36718-112">PARAMETERS</span></span>

### <span data-ttu-id="36718-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="36718-113">-CertName</span></span>
<span data-ttu-id="36718-114">KeyVaultCertName do certificado criado em keyvault</span><span class="sxs-lookup"><span data-stu-id="36718-114">KeyVaultCertName of the certificate created in keyvault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36718-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36718-115">-DefaultProfile</span></span>
<span data-ttu-id="36718-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36718-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36718-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="36718-117">-KeyVaultName</span></span>
<span data-ttu-id="36718-118">O nome do keyvault.</span><span class="sxs-lookup"><span data-stu-id="36718-118">The name of the keyvault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36718-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36718-119">-ResourceGroupName</span></span>
<span data-ttu-id="36718-120">O nome do grupo de recursos webapp.</span><span class="sxs-lookup"><span data-stu-id="36718-120">The name of the webapp resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36718-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="36718-121">-Slot</span></span>
<span data-ttu-id="36718-122">O nome do slot do webapp.</span><span class="sxs-lookup"><span data-stu-id="36718-122">The name of the webapp slot.</span></span>

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

### <span data-ttu-id="36718-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="36718-123">-WebAppName</span></span>
<span data-ttu-id="36718-124">O nome do webapp.</span><span class="sxs-lookup"><span data-stu-id="36718-124">The name of the webapp.</span></span>

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

### <span data-ttu-id="36718-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36718-125">-Confirm</span></span>
<span data-ttu-id="36718-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36718-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36718-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36718-127">-WhatIf</span></span>
<span data-ttu-id="36718-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36718-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36718-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36718-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36718-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36718-130">CommonParameters</span></span>
<span data-ttu-id="36718-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36718-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36718-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36718-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36718-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36718-133">INPUTS</span></span>

### <span data-ttu-id="36718-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="36718-134">None</span></span>

## <span data-ttu-id="36718-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="36718-135">OUTPUTS</span></span>

### <span data-ttu-id="36718-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="36718-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="36718-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="36718-137">NOTES</span></span>

## <span data-ttu-id="36718-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36718-138">RELATED LINKS</span></span>
