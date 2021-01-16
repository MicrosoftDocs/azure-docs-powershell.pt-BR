---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271229"
---
# <span data-ttu-id="72dd8-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="72dd8-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="72dd8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="72dd8-103">Adiciona um certificado de criptografia de dados transparente para a instância gerenciada fornecida</span><span class="sxs-lookup"><span data-stu-id="72dd8-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="72dd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72dd8-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72dd8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72dd8-105">DESCRIPTION</span></span>
<span data-ttu-id="72dd8-106">O Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adiciona um certificado de criptografia de dados transparente para a instância gerenciada fornecida</span><span class="sxs-lookup"><span data-stu-id="72dd8-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="72dd8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72dd8-107">EXAMPLES</span></span>

### <span data-ttu-id="72dd8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72dd8-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="72dd8-109">OS</span><span class="sxs-lookup"><span data-stu-id="72dd8-109">PARAMETERS</span></span>

### <span data-ttu-id="72dd8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72dd8-110">-DefaultProfile</span></span>
<span data-ttu-id="72dd8-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72dd8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72dd8-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="72dd8-112">-ManagedInstanceName</span></span>
<span data-ttu-id="72dd8-113">O nome da instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="72dd8-113">The managed instance name</span></span>

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

### <span data-ttu-id="72dd8-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72dd8-114">-PassThru</span></span>
<span data-ttu-id="72dd8-115">Na execução bem-sucedida, retorna o objeto de certificado que foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="72dd8-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="72dd8-116">-Senha</span><span class="sxs-lookup"><span data-stu-id="72dd8-116">-Password</span></span>
<span data-ttu-id="72dd8-117">A senha para certificado de criptografia de dados transparente</span><span class="sxs-lookup"><span data-stu-id="72dd8-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dd8-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="72dd8-118">-PrivateBlob</span></span>
<span data-ttu-id="72dd8-119">O blob privado para certificado de criptografia de dados transparente</span><span class="sxs-lookup"><span data-stu-id="72dd8-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dd8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72dd8-120">-ResourceGroupName</span></span>
<span data-ttu-id="72dd8-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="72dd8-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="72dd8-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72dd8-122">-Confirm</span></span>
<span data-ttu-id="72dd8-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72dd8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72dd8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72dd8-124">-WhatIf</span></span>
<span data-ttu-id="72dd8-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72dd8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72dd8-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72dd8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72dd8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72dd8-127">CommonParameters</span></span>
<span data-ttu-id="72dd8-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72dd8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72dd8-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72dd8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72dd8-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72dd8-130">INPUTS</span></span>

### <span data-ttu-id="72dd8-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="72dd8-131">None</span></span>

## <span data-ttu-id="72dd8-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72dd8-132">OUTPUTS</span></span>

### <span data-ttu-id="72dd8-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72dd8-133">System.Boolean</span></span>

## <span data-ttu-id="72dd8-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72dd8-134">NOTES</span></span>

## <span data-ttu-id="72dd8-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72dd8-135">RELATED LINKS</span></span>
