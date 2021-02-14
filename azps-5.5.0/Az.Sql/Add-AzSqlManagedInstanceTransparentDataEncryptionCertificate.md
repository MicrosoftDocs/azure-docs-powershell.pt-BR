---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111351"
---
# <span data-ttu-id="9a559-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="9a559-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="9a559-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a559-102">SYNOPSIS</span></span>
<span data-ttu-id="9a559-103">Adiciona um Certificado de Criptografia de Dados Transparente para uma determinada instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="9a559-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="9a559-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a559-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a559-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a559-105">DESCRIPTION</span></span>
<span data-ttu-id="9a559-106">O Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adiciona um Certificado de Criptografia de Dados Transparentes para uma determinada instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="9a559-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="9a559-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a559-107">EXAMPLES</span></span>

### <span data-ttu-id="9a559-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a559-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="9a559-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a559-109">PARAMETERS</span></span>

### <span data-ttu-id="9a559-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a559-110">-DefaultProfile</span></span>
<span data-ttu-id="9a559-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a559-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a559-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="9a559-112">-ManagedInstanceName</span></span>
<span data-ttu-id="9a559-113">O nome da instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="9a559-113">The managed instance name</span></span>

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

### <span data-ttu-id="9a559-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a559-114">-PassThru</span></span>
<span data-ttu-id="9a559-115">Em Execução bem-sucedida, retorna o objeto de certificado que foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="9a559-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="9a559-116">-Senha</span><span class="sxs-lookup"><span data-stu-id="9a559-116">-Password</span></span>
<span data-ttu-id="9a559-117">A senha do certificado de criptografia de dados transparentes</span><span class="sxs-lookup"><span data-stu-id="9a559-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="9a559-118">-PrivateB ltd</span><span class="sxs-lookup"><span data-stu-id="9a559-118">-PrivateBlob</span></span>
<span data-ttu-id="9a559-119">O blob particular para certificado de criptografia de dados transparentes</span><span class="sxs-lookup"><span data-stu-id="9a559-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="9a559-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a559-120">-ResourceGroupName</span></span>
<span data-ttu-id="9a559-121">O Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="9a559-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="9a559-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9a559-122">-Confirm</span></span>
<span data-ttu-id="9a559-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a559-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a559-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a559-124">-WhatIf</span></span>
<span data-ttu-id="9a559-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9a559-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a559-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a559-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a559-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a559-127">CommonParameters</span></span>
<span data-ttu-id="9a559-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a559-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a559-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a559-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a559-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="9a559-130">INPUTS</span></span>

### <span data-ttu-id="9a559-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9a559-131">None</span></span>

## <span data-ttu-id="9a559-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="9a559-132">OUTPUTS</span></span>

### <span data-ttu-id="9a559-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a559-133">System.Boolean</span></span>

## <span data-ttu-id="9a559-134">Notas</span><span class="sxs-lookup"><span data-stu-id="9a559-134">NOTES</span></span>

## <span data-ttu-id="9a559-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a559-135">RELATED LINKS</span></span>
