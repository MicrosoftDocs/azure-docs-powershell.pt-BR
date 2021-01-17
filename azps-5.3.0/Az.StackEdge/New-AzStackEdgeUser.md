---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427002"
---
# <span data-ttu-id="44abc-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="44abc-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="44abc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44abc-102">SYNOPSIS</span></span>
<span data-ttu-id="44abc-103">Cria um novo usuário para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44abc-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="44abc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44abc-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44abc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44abc-105">DESCRIPTION</span></span>
<span data-ttu-id="44abc-106">O cmdlet **New-AzStackEdgeUser** cria um novo usuário para o dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="44abc-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="44abc-107">Só há suporte para a criação de usuários do tipo `Share` .</span><span class="sxs-lookup"><span data-stu-id="44abc-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="44abc-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44abc-108">EXAMPLES</span></span>

### <span data-ttu-id="44abc-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44abc-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="44abc-110">OS</span><span class="sxs-lookup"><span data-stu-id="44abc-110">PARAMETERS</span></span>

### <span data-ttu-id="44abc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44abc-111">-AsJob</span></span>
<span data-ttu-id="44abc-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="44abc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44abc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44abc-113">-DefaultProfile</span></span>
<span data-ttu-id="44abc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44abc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44abc-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="44abc-115">-DeviceName</span></span>
<span data-ttu-id="44abc-116">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="44abc-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44abc-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="44abc-117">-EncryptionKey</span></span>
<span data-ttu-id="44abc-118">Chave de criptografia do dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="44abc-118">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44abc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="44abc-119">-Name</span></span>
<span data-ttu-id="44abc-120">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="44abc-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44abc-121">-Senha</span><span class="sxs-lookup"><span data-stu-id="44abc-121">-Password</span></span>
<span data-ttu-id="44abc-122">Senha, fornecer como uma cadeia de caracteres segura</span><span class="sxs-lookup"><span data-stu-id="44abc-122">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44abc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44abc-123">-ResourceGroupName</span></span>
<span data-ttu-id="44abc-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="44abc-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44abc-125">-Digite</span><span class="sxs-lookup"><span data-stu-id="44abc-125">-Type</span></span>
<span data-ttu-id="44abc-126">Selecionar UserType</span><span class="sxs-lookup"><span data-stu-id="44abc-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44abc-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44abc-127">-Confirm</span></span>
<span data-ttu-id="44abc-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44abc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44abc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44abc-129">-WhatIf</span></span>
<span data-ttu-id="44abc-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44abc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44abc-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44abc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44abc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44abc-132">CommonParameters</span></span>
<span data-ttu-id="44abc-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44abc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44abc-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44abc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44abc-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44abc-135">INPUTS</span></span>

### <span data-ttu-id="44abc-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="44abc-136">None</span></span>

## <span data-ttu-id="44abc-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44abc-137">OUTPUTS</span></span>

### <span data-ttu-id="44abc-138">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="44abc-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="44abc-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44abc-139">NOTES</span></span>

## <span data-ttu-id="44abc-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44abc-140">RELATED LINKS</span></span>
